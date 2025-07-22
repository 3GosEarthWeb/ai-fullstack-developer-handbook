# Deployment Prompts

Use these AI-powered prompts to automate, scaffold, and debug deployment pipelines for fullstack applications. They cover Docker, CI/CD, cloud hosting, and infrastructure-as-code.

---

## 🐳 Docker Prompts

**1. Basic Dockerfile**

```
Write a Dockerfile for a FastAPI app using `uvicorn` and `requirements.txt`. Use python:3.11-slim.
```

**2. Multi-stage Build Prompt**

```
Generate a multi-stage Dockerfile for a React frontend (Vite) + FastAPI backend.
```

**3. Docker Compose Prompt**

```
Create a docker-compose.yml with services for: backend (FastAPI), frontend (React), db (PostgreSQL), and adminer.
```

---

## ⚙️ GitHub Actions / CI Prompts

**4. FastAPI Test & Deploy CI**

```
Write a GitHub Actions workflow that installs Python, runs FastAPI tests with `pytest`, then deploys if all tests pass.
```

**5. Fullstack CI Prompt**

```
Generate a GitHub Actions pipeline that:
- Lints backend Python code
- Builds frontend React app
- Runs Supabase migrations
- Deploys to Render/Vercel on push to main
```

---

## ☁️ Hosting Platform Prompts

**6. Render Deployment Prompt**

```
Write steps to deploy a FastAPI app to Render.com using GitHub integration and environment variables.
```

**7. Vercel Frontend Prompt**

```
Deploy a React Vite app to Vercel with custom environment variables and a preview URL for each PR.
```

---

## 🔐 Secrets & Config Prompts

**8. Supabase Environment Prompt**

```
List required environment variables to deploy a fullstack app using Supabase, FastAPI, and React.
```

**9. GitHub Secrets Prompt**

```
How do I securely store and use my `SUPABASE_KEY`, `DATABASE_URL`, and `OPENAI_API_KEY` in GitHub Actions?
```

---

## 📦 Deployment with Infrastructure as Code (IaC)

**10. Terraform Prompt**

```
Generate a Terraform script to deploy a PostgreSQL DB on Supabase and a FastAPI backend on Render.
```

**11. Ansible Prompt**

```
Create an Ansible playbook to deploy a fullstack app (React + FastAPI) to an Ubuntu server.
```

---

## 🚦Health Checks & Monitoring

**12. Health Check Prompt**

```
Write a FastAPI `/health` endpoint and add it to a Render/Vercel health check path.
```

**13. Uptime Monitoring Prompt**

```
Suggest how to use UptimeRobot or Grafana to monitor my deployed app’s availability and response times.
```

---

## 💡 Bonus Prompts for DevOps Agents

**14. DevOps Agent Prompt**

```
Create a DevOps agent using AutoGen that:
- Reads app directory structure
- Builds Docker containers
- Tests with CI
- Deploys to Render
```

**15. Rollback Plan Prompt**

```
Write a GitHub Action step that rolls back a deployment if the health check fails after deploy.
```

---

## ✅ Deployment Checklist Prompt

```
Generate a deployment checklist for a fullstack app that includes:
- Build + test frontend
- Build backend container
- Migrate database
- Deploy backend
- Deploy frontend
- Verify env variables
- Add uptime monitoring
```

---

These prompts help ship your code with confidence. Use them in VS Code Copilot, ChatGPT, or integrate into your AI agent flow.

Next up: explore how to manage production access, secrets, and alerting in `Chapter: 09-auth-security` and `Chapter: 12-admin-analytics`.

