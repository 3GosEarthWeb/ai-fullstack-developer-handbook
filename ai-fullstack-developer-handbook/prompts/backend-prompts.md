# Backend Prompts

This chapter provides powerful prompt templates and examples for generating, testing, and deploying backend services using AI tools like GPT-4, Claude, or open-source LLMs.

---

## ⚙️ API Development Prompts

**1. CRUD API Prompt**

```
Write FastAPI CRUD endpoints for a `Transaction` model with fields: id, user_id, amount, type, timestamp.
```

**2. Auth Routes Prompt**

```
Create FastAPI endpoints for user signup and login with JWT authentication. Use password hashing with bcrypt.
```

**3. Validated Input Prompt**

```
Generate a FastAPI POST endpoint to accept a loan application. Validate fields like amount (min 1000), duration (1–36 months), and income (required).
```

---

## 🔐 Auth & Security Prompts

**4. OAuth Login Prompt**

```
Add Google OAuth login to a FastAPI backend using `authlib` or `fastapi-users`.
```

**5. RBAC Prompt**

```
Implement role-based access control (RBAC) in FastAPI. Only users with 'admin' role should access /admin routes.
```

---

## 🧪 Testing & Debugging Prompts

**6. Pytest Prompt**

```
Write Pytest unit tests for a FastAPI route that transfers money between two accounts.
```

**7. Bug Fix Prompt**

```
Here's my FastAPI POST route for /deposit. It fails when amount is 0. Fix the issue and add error handling.
```

---

## 🗃️ Supabase/SQL Prompts

**8. Supabase Schema Prompt**

```
Generate SQL for a Supabase table `accounts` with fields: id (UUID), user_id (FK), balance, type (savings/current), created_at.
```

**9. Policy Prompt**

```
Create Supabase RLS policies to allow only the owner of a row to update their account.
```

---

## 🚀 Deployment Prompts

**10. Docker Prompt**

```
Create a Dockerfile for a FastAPI backend with requirements.txt and a uvicorn entrypoint.
```

**11. Render Deploy Prompt**

```
Write steps to deploy a FastAPI backend with PostgreSQL to Render.com.
```

---

## 🧠 Backend Agent Prompts

**12. AutoGen Agent Prompt**

```
Create an AutoGen agent that receives a bug report and rewrites the broken backend endpoint using FastAPI.
```

**13. CrewAI Agent Prompt**

```
Create a CrewAI team with a BackendAgent to build the API and a ReviewerAgent to lint and test each route.
```

---

## 📦 Extra Prompts

- Generate a FastAPI health check route at `/health` that returns `status: ok`.
- Write a FastAPI middleware that logs every request path and status.
- Create an endpoint to return paginated results from a `transactions` table.

---

## ✅ Best Practices Prompts

**14. Error Handling Prompt**

```
Show a reusable FastAPI exception handler for 404 and 500 errors with JSON responses.
```

**15. Logging Prompt**

```
Add a logging config in FastAPI that logs errors to a file and console with timestamp.
```

---

## 📂 Bonus: Prompt Template File

You can save prompts like this to a `.prompt.json` or `.prompt.md` file and load them dynamically into your AI toolchain or prompt manager.

```
{
  "name": "Generate Transaction API",
  "prompt": "Write a POST route in FastAPI that transfers funds securely between two accounts."
}
```

---

Ready to generate code?

Use these prompts directly in ChatGPT, Claude, or integrate with your dev agent system.
