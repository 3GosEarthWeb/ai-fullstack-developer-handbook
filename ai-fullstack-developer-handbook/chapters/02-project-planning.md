# Chapter 2: Project Planning with AI

## 🧠 Why Use AI for Planning?

AI can dramatically accelerate the early stages of your project:

- Generate app ideas based on goals or industries
- Choose the most efficient tech stack
- Design folder structures and system architecture
- Break the app into manageable tasks (MVP scope)

With proper prompting, AI becomes your **project manager + tech architect**.

## 📝 Step 1: Define the Project with a Prompt

Use natural language to describe your idea. Example prompt:

> I want to build a web-based banking app for customers and admins. It should allow account management, fund transfers, loan applications, and display dashboards. Use React for frontend, FastAPI for backend, Supabase for the database.

🔍 **What AI returns:**

- Stack recommendation: React + Vite, FastAPI, Supabase
- API routes: `/auth`, `/accounts`, `/transactions`, `/loans`
- Database schema suggestions
- Suggested folders: `components/`, `services/`, `routes/`, `models/`

## 🧱 Step 2: Choose Your Tech Stack

Let AI evaluate your needs:

> **Prompt**:  
> Suggest the best stack for a mobile-friendly banking dashboard with user authentication, role-based access, and analytics. Use modern tools and keep it lightweight.

✅ **Expected Stack Output:**

- **Frontend**: React + Vite + Bootstrap/Tailwind
- **Backend**: FastAPI (Python) or Node.js (Express)
- **Database**: Supabase (PostgreSQL)
- **Auth**: JWT
- **Deployment**: Vercel (frontend), Railway/Fly.io (backend)
- **CI/CD**: GitHub Actions

## 📂 Step 3: Scaffold File & Folder Structure

Ask:

> Generate a clean folder structure for a fullstack app with React frontend and FastAPI backend, using Supabase as the DB.

📁 Example Output:

```bash
project-root/
├── frontend/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       └── App.jsx
├── backend/
│   ├── app/
│   │   ├── routes/
│   │   ├── models/
│   │   └── main.py
├── database/
│   └── schema.sql
├── docker-compose.yml
└── README.md
```

You can then run a script to generate these folders automatically.

## ✅ Step 4: Define the MVP

> Break this project into an MVP version with key features only.

🛠 AI Response:

### ✅ MVP Features

- User signup/login
- View account balance
- Deposit, withdraw, transfer
- Apply for a loan
- Admin: approve/reject loans
- Responsive dashboard

📋 Tasks breakdown (example):

1. Setup Supabase with tables  
2. Build FastAPI routes for auth/accounts  
3. Create React login + dashboard page  
4. Add Axios services for API calls  
5. Deploy frontend & backend

## ⌛ Step 5 - Generate Agile Tasks

Use prompts like:

> Turn the MVP into a list of agile development tasks with user stories and estimated time.

Example Output:

```markdown
- [ ] As a user, I want to sign up and log in (2h)
- [ ] As a user, I want to view my account balance (1h)
- [ ] As an admin, I want to approve loan applications (3h)
```

## 🧠 Prompt Templates for Planning

Here are reusable planning prompts:

- `Brainstorm`:  
  _Suggest 3 SaaS ideas I can build in a weekend using AI tools._

- `Architecture`:  
  _Design a modular fullstack app with auth, dashboards, and analytics. Use React, FastAPI, and Supabase._

- `Scaffolding`:  
  _Generate a file structure for a fullstack finance dashboard app._

- `Task Breakdown`:  
  _Break down the MVP into technical tasks with estimated time._

## 🔁 Iterate with AI

The best way to plan with AI:

1. Start broad → “Design a SaaS finance app”  
2. Get structure → “Create backend API routes”  
3. Get tasks → “Break into development stages”  
4. Refine → “Focus on role-based auth and deployment”

## 📦 Up Next

### Chapter 3 – Prompt Engineering

Learn how to write:

- System prompts  
- Task-specific dev prompts  
- Iterative and context-aware queries

> 📍 File: [`03-prompt-engineering.md`](./03-prompt-engineering.md)
