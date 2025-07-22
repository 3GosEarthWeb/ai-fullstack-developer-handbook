# Chapter 3: Prompt Engineering

## 🧠 What is Prompt Engineering?

**Prompt engineering** is the skill of crafting input text that guides AI models (like ChatGPT) to generate accurate, helpful, and context-aware output.

Just like good code leads to reliable apps, good prompts lead to powerful AI responses.

## 🎯 Why Prompt Engineering Matters in Development

As a fullstack developer using AI, your **prompts become code instructions**. They define:

- What the AI builds (UI, API, tests, docs)
- How the AI reasons (step-by-step logic vs output dump)
- How well it understands context (project scope, roles, tech stack)

Well-crafted prompts = faster, cleaner, and safer code.

## ✍️ Prompt Types for Fullstack Dev

| Type                | Example Use                                  |
|---------------------|----------------------------------------------|
| **Descriptive**     | "Create a login form using React + Bootstrap" |
| **Instructional**   | "Write a FastAPI POST route for /accounts"    |
| **Architectural**   | "Design a scalable folder structure for a SaaS app" |
| **Iterative**       | "Refactor the previous code to use async/await" |
| **Checklist-based** | "List all validation rules for a sign-up form" |

## 🧪 Prompt Formula — DEV + CONTEXT + OUTPUT

```text
As a [role], build [what] using [tools or constraints].
Include [features or details], output only [code/markdown/json/etc.].
```

### 🔧 Example

> As a backend engineer, build an endpoint to transfer funds between users using FastAPI and SQLAlchemy. Include input validation, transaction safety, and return a JSON response. Output only the Python code.

## 🧠 Prompt Engineering Patterns

### 1. System Prompts

Set the AI’s persona and style:

```text
You are a senior fullstack engineer.
Be concise and accurate. Explain your code.
```

### 2. Few-Shot Prompting

Give 1–2 examples, then ask AI to continue the pattern.

```markdown
Input: Login form using React  
Output:
```jsx
function LoginForm() {
  return <form>{/* login UI */}</form>;
}

Input: Registration form  
Output:

### 3. Step-by-Step Prompts

```markdown
- First, generate Supabase tables.
- Then, write FastAPI routes.
- Finally, return a sample JSON response.
```

## 📦 Common Dev Prompts (Cheat Sheet)

### ✅ Frontend

```text
Build a responsive user dashboard in React using Bootstrap.
Include: profile card, balance summary, recent transactions list.
```

### ✅ Backend

```text
Generate a FastAPI route to handle loan applications.
Fields: amount, term, user_id. Save to PostgreSQL via SQLAlchemy.
```

### ✅ Database

```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  password_hash TEXT NOT NULL
);
```

### ✅ Deployment

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

## ⚠️ Prompt Mistakes to Avoid

- ❌ Too vague: “Build an app” → Confusing
- ❌ No constraints: “Use any stack” → Unpredictable
- ❌ No format: “Give me the code” → No language or structure
- ❌ No context: “Fix this code” → Without showing the code

✅ Always specify:

- Role + Task
- Stack or tools
- Format (code, JSON, Markdown, etc.)
- Constraints (time, features, security, etc.)

## 📂 Prompt Storage Strategy

Organize your prompts in your project like this:

/prompts
  ├── frontend-prompts.md
  ├── backend-prompts.md
  ├── auth-prompts.md
  ├── deployment-prompts.md
  └── agent-prompts.md

Use version control to evolve your best prompts over time.

## 🚀 Bonus: Turn Prompts into Tools

Use tools like:

- **LangChain** to turn prompts into agent actions
- **Promptable** or **OpenPrompt** to test and manage prompt variations
- **VS Code Snippets** to reuse top prompts instantly

## 🧭 Up Next: Chapter 4 – System Design with AI

Learn how to:

- Build architecture diagrams with prompts
- Model services and modules with AI
- Balance frontend/backend responsibility with LLMs

> 📍 File: [`04-system-design.md`](./04-system-design.md)
