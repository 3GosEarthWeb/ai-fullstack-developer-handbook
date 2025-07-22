# Chapter 4: System Design with AI

## 🧱 What is System Design?

System design is the process of defining the architecture, components, modules, interfaces, and data flow of a software system.

With the help of AI, this traditionally complex task becomes faster and more collaborative.

**AI can help you:**

- Draft scalable architectures
- Choose protocols (REST, WebSocket, gRPC)
- Visualize system workflows
- Suggest performance and security strategies

---

## 🎯 Why Use AI for System Design?

Prompting AI in the early stages helps:

- Reduce decision fatigue
- Explore multiple patterns quickly
- Bootstrap architecture docs
- Align frontend/backend planning

---

## 🧠 Prompt Formula for System Design

Design a scalable [type] system for [use-case] using [tools].
Include modules for [features]. Describe data flow, services, and responsibilities.

### Example Prompt

> Design a scalable architecture for a fullstack online banking app.  
> Use React for frontend, FastAPI for backend, Supabase for database, and JWT for auth.  
> Include modules for account management, transactions, loans, and user roles.

---

## 🧩 AI-Generated System Breakdown

Client → React Frontend → FastAPI → Supabase (PostgreSQL)

Modules:
- Auth Service
- Account Service
- Transaction Service
- Loan Service
- Admin Module

Flow:
1. Client sends a request to FastAPI
2. FastAPI validates JWT and routes to correct module
3. Module queries Supabase
4. Response is sent back to frontend

---

## 🗂 Example Folder Structure (Fullstack App)

project-root/
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── api/
│   │   ├── models/
│   │   ├── services/
│   │   └── auth/
├── frontend/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── context/
│       └── App.jsx
├── docker-compose.yml
└── README.md

---

## 🔐 Security Guidelines

> Prompt: What security should I implement for a FastAPI + Supabase banking app?

AI should suggest:

- HTTPS + secure cookies
- JWT expiration and refresh
- Role-based access control (RBAC)
- Input validation (backend and frontend)
- Audit logs
- Rate limiting + monitoring

---

## ⚙️ Scaling with AI Help

> Prompt: How do I scale my banking app to support 10,000 users?

AI typically replies:

- Use async routes (FastAPI)
- Enable PostgreSQL connection pooling
- Deploy with autoscaling (Railway, Render, Fly.io)
- Serve static frontend via CDN (Cloudflare, Vercel)
- Cache frequent queries (Redis, Supabase edge functions)

---

## 📈 System Design Diagram (ASCII Style)

  [Browser]
      |
      V
  [React UI]
      |
      V
   [FastAPI]
 ┌──────────────┬──────────────┬──────────────┐
 │   Accounts   │ Transactions │     Loans    │
 └──────┬───────┴───────┬──────┴───────┬──────┘
        V               V              V
              [Supabase PostgreSQL]
> Copy this into GitHub README or use tools like Excalidraw or Lucidchart for visuals.

---

## 🔁 Common System Design Prompts

- **"Design a microservice-based backend for a banking app using FastAPI."**
- **"Suggest a folder structure for a React + FastAPI monorepo."**
- **"How would you implement multi-tenancy in Supabase?"**
- **"What monitoring tools should I add to my Python backend?"**

---

## ✅ Tips for AI-Assisted Design

- Ask role-specific prompts (e.g., "As an SRE...")
- Be clear about tools and scale
- Request step-by-step responses
- Ask for visual summaries or ASCII diagrams
- Store AI-generated system designs in version control

---

## ⏭ Next: Chapter 5 – Building AI Agents

Learn how to:

- Use LangChain or CrewAI for multi-agent setups
- Give agents memory, tools, and planning logic
- Connect prompts to workflows, tasks, and APIs

> 📂 File: [`05-building-ai-agents.md`](./05-building-ai-agents.md)
