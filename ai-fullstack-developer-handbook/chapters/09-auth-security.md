# Chapter 9: Authentication & Security

## 🔐 Why It Matters

Authentication (auth) verifies user identity. Security protects your app, data, and users from threats. Together, they ensure:

- Only the right users get access
- Data stays private and trusted
- Attacks like SQL injection, XSS, and CSRF are mitigated

---

## 🤖 How AI Assists in Auth & Security

AI tools can:

- Scaffold complete auth flows
- Suggest secure password handling
- Generate JWT/OAuth logic
- Explain security risks in your code
- Help write RLS (Row-Level Security) policies in Supabase

---

## 🧠 Prompt Formula for Auth Tasks

```
Create [auth flow] in [framework] with [method] and [security mechanism].
```

### ✅ Example Prompt

> Create a FastAPI login and signup flow using JWT and Pydantic. Hash passwords with bcrypt.

---

## 🔑 Types of Authentication

| Type            | Description                            | Example Use     |
|------------------|----------------------------------------|------------------|
| Username/Password | Basic form with hashed passwords       | Most logins      |
| JWT              | Token-based, stateless auth             | APIs, mobile apps |
| OAuth 2.0        | Login with Google/Facebook etc.         | Social login     |
| Magic Link       | One-click email login                   | Passwordless     |
| 2FA              | Extra security layer with code          | Banking apps     |

---

## 🔐 Implementing JWT Auth (FastAPI Example)

```python
from fastapi import FastAPI, Depends, HTTPException
from jose import JWTError, jwt
from datetime import datetime, timedelta

SECRET_KEY = "your-secret"
ALGORITHM = "HS256"

def create_access_token(data: dict, expires_delta: timedelta):
    to_encode = data.copy()
    expire = datetime.utcnow() + expires_delta
    to_encode.update({"exp": expire})
    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)
```

Prompt:

> Generate FastAPI middleware to decode and verify JWT from the `Authorization` header.

---

## 🔒 Password Hashing with bcrypt

```python
from passlib.context import CryptContext

pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")

def hash_password(password: str) -> str:
    return pwd_context.hash(password)

def verify_password(plain_password: str, hashed_password: str) -> bool:
    return pwd_context.verify(plain_password, hashed_password)
```

Prompt:

> Implement password hashing and verification in Python using bcrypt.

---

## 🛡 Supabase Row Level Security (RLS)

Use RLS to ensure users can access only their data.

Prompt:

> Write a Supabase RLS policy to allow a user to access only their own accounts table row.

```sql
-- Policy
CREATE POLICY "Users can read their own accounts"
  ON accounts
  FOR SELECT
  USING (auth.uid() = user_id);
```

---

## 🚨 Security Best Practices

- ✅ Hash passwords before storing
- ✅ Use HTTPS (SSL/TLS)
- ✅ Sanitize all inputs
- ✅ Use `.env` for secrets
- ✅ Avoid exposing stack traces
- ✅ Rate-limit API requests

Prompt:

> List 10 security tips for building a secure fullstack app with FastAPI and Supabase.

---

## 🔐 OAuth2 Example (Login with GitHub)

Use libraries like `authlib`, `passport`, or Supabase built-in auth.

Prompt:

> Set up GitHub login using OAuth2 in a FastAPI project with Authlib.

---

## 🔍 Testing Auth & Security

Use tools like:

- `pytest` for login/logout tests
- `OWASP ZAP` or `Burp Suite` for vulnerability scanning
- AI for static code analysis

Prompt:

> Write a test case to validate token expiry and invalid JWT rejection.

---

## 🧪 Checklist for Secure Auth

- [x] Passwords are hashed
- [x] JWTs are signed and expiring
- [x] Secrets are in `.env`
- [x] Login is rate-limited
- [x] Role-based access enforced
- [x] Auth tested with edge cases

---

## 🧭 Up Next: Chapter 10 – AI Agents & Automation

Explore:

- LangChain, CrewAI, and AutoGen
- Creating autonomous agents for code, testing, and deployment
- Letting AI act like a dev teammate

> 📂 File: [`10-ai-agents.md`](./10-ai-agents.md)
