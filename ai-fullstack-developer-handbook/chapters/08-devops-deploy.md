# Chapter 8: DevOps & Deployment

## 🚀 What is DevOps?

**DevOps** is the practice of integrating **development** and **operations** to automate and streamline the process of:

- Building
- Testing
- Releasing
- Monitoring

DevOps ensures faster and safer delivery of software with automation, continuous integration (CI), and continuous deployment (CD).

---

## 🤖 How AI Assists DevOps

AI tools can:

- Auto-generate GitHub Actions workflows
- Suggest Dockerfiles
- Analyze logs and recommend fixes
- Optimize infrastructure costs
- Write CI/CD pipelines with prompts

---

## 🧠 Prompt Formula for DevOps Tasks

```
Generate a CI/CD pipeline for [framework] using [platform].
Include steps for [test, lint, build, deploy].
```

### ✅ Example Prompt

> Write a GitHub Actions workflow to lint, test, and deploy a FastAPI + Vite project to Railway.

---

## 🧰 Tools in the DevOps Stack

| Area         | Tool / Platform       |
|--------------|------------------------|
| Versioning   | Git, GitHub            |
| CI/CD        | GitHub Actions, GitLab CI |
| Container    | Docker                 |
| Deployment   | Railway, Fly.io, Render |
| Monitoring   | LogRocket, Grafana, Sentry |
| Secrets Mgmt | GitHub Secrets, Dotenv |

---

## 🐳 Docker Setup Example

```dockerfile
# Dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
```

Prompt:

> Generate a Dockerfile for a FastAPI backend with Uvicorn and auto-reload support.

---

## 🔁 GitHub Actions CI/CD Example

```yaml
# .github/workflows/deploy.yml
name: CI/CD

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'

      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt

      - name: Run Tests
        run: pytest

      - name: Deploy to Railway
        run: railway up
```

Prompt:

> Write a GitHub Action to test and deploy a FastAPI project to Railway when I push to main.

---

## 🛡 Secrets Management

Do **not** hardcode secrets.

Use tools like:

- `.env` + `python-dotenv`
- GitHub Secrets
- Supabase Vault

Prompt:

> How do I securely load secrets in a FastAPI app using dotenv?

---

## 📦 Deployment Platforms

- [Railway](https://railway.app/)
- [Fly.io](https://fly.io/)
- [Render](https://render.com/)
- [Supabase Edge Functions](https://supabase.com/docs/guides/functions)

Prompt:

> Deploy my fullstack app (FastAPI + Vite) to Render with HTTPS and environment variables.

---

## 📊 Monitoring & Observability

Track app health and logs with:

- [Sentry](https://sentry.io/)
- [LogRocket](https://logrocket.com/)
- [Grafana](https://grafana.com/)
- [Prometheus](https://prometheus.io/)

Prompt:

> Suggest monitoring tools for my FastAPI backend with alerts and error tracking.

---

## 🧪 Testing in CI

Test your backend and frontend automatically on every push.

Prompt:

> Add a test step to my GitHub Action for a React frontend using `vitest`.

---

## 📁 Project Folder with DevOps

```
project-root/
├── frontend/
├── backend/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── Dockerfile
├── docker-compose.yml
├── .env
└── README.md
```

---

## 🧭 Up Next: Chapter 9 – AI Agents & Automation

Explore how to:

- Use agents like LangChain or CrewAI
- Orchestrate workflows that call APIs
- Let AI manage routine developer tasks

> 📂 File: [`09-ai-agents.md`](./09-ai-agents.md)
