# Chapter 7: Database Schema & Integration

## 🗄 What is a Database?

A database is a structured system for storing and retrieving data. In fullstack development, it powers everything from user logins to transaction histories.

Backend services communicate with databases to:

- Store structured data (e.g., users, accounts, logs)
- Retrieve and filter records
- Manage relationships between entities

---

## ⚙️ Choosing a Database

For modern fullstack apps, choose based on:

| Use Case         | Recommended DB      |
|------------------|---------------------|
| Relational       | PostgreSQL (via Supabase) |
| Realtime sync    | Supabase Realtime   |
| Caching/Queueing | Redis               |
| Search           | Meilisearch / Typesense |

Prompt Example:

> What’s the best database setup for a banking app with transaction logs, role-based users, and loan repayments?

---

## 🧠 Prompt Formula for Schema Design

```
Design a relational database schema for [domain].
Include tables for [entities] with relationships and constraints.
Use [SQL/PostgreSQL] format.
```

### ✅ Example Prompt

> Design a PostgreSQL schema for an online banking system. Include tables for users, accounts, transactions, loans, repayments, and roles. Enforce relationships.

---

## 🏗 Sample Schema (Banking App)

```sql
-- Users Table
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email TEXT UNIQUE NOT NULL,
  full_name TEXT,
  password_hash TEXT NOT NULL,
  role TEXT CHECK (role IN ('customer', 'admin')) DEFAULT 'customer',
  created_at TIMESTAMP DEFAULT NOW()
);

-- Accounts Table
CREATE TABLE accounts (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  account_type TEXT CHECK (account_type IN ('savings', 'current')),
  balance NUMERIC DEFAULT 0,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Transactions Table
CREATE TABLE transactions (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  account_id UUID REFERENCES accounts(id),
  type TEXT CHECK (type IN ('deposit', 'withdrawal', 'transfer')),
  amount NUMERIC NOT NULL,
  reference TEXT,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Loans Table
CREATE TABLE loans (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  amount NUMERIC NOT NULL,
  status TEXT CHECK (status IN ('pending', 'approved', 'rejected')) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT NOW()
);

-- Loan Repayments
CREATE TABLE loan_repayments (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  loan_id UUID REFERENCES loans(id),
  amount NUMERIC,
  paid_on TIMESTAMP DEFAULT NOW()
);
```

---

## 🧩 Normalization & Best Practices

- Use UUIDs for primary keys
- Use foreign keys to ensure referential integrity
- Apply `CHECK` constraints for enums
- Store timestamps for audit/logging
- Index frequently queried columns

---

## 🔁 Migrations

Prompt:

> Generate Alembic migration for creating `accounts` and `transactions` tables in FastAPI.

AI will scaffold versioned migration scripts for schema evolution.

---

## 🔄 Supabase Integration

- Use SQL Editor for schema
- Use Supabase dashboard for browsing rows
- Supabase client SDK (JS, Python) for CRUD
- Use Row Level Security (RLS) to control access

Prompt:

> Generate a Supabase RLS policy that allows users to read only their own `accounts`.

---

## ✅ Schema Testing Tips

Prompt:

> How can I test my PostgreSQL schema during backend development?

Recommendations include:

- Use `pytest-postgresql` or Docker test containers
- Seed test data with fixtures
- Test constraint violations (e.g., foreign key, null)

---

## 🧭 Up Next: Chapter 8 – Authentication & Security

We’ll cover:

- Auth flows with FastAPI and JWT
- OAuth with Supabase
- Role-based access control (RBAC)
- AI prompts for securing APIs and DB access

> 📂 File: [`08-authentication.md`](./08-authentication.md)
