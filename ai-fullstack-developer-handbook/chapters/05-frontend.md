# Chapter 5: Frontend Development with AI

## 🎨 What is Frontend Development?

Frontend development involves building the **user interface (UI)** and **user experience (UX)** of web applications — the parts users interact with directly.

As a fullstack developer, your frontend work includes:

- Designing responsive layouts
- Implementing interactivity with JavaScript frameworks
- Integrating APIs
- Ensuring accessibility and performance

---

## 🤖 How AI Enhances Frontend Work

AI tools like ChatGPT, GitHub Copilot, and Codeium can:

- Generate components and layouts in React, Vue, or Svelte
- Suggest CSS or Tailwind classes
- Refactor UI logic
- Improve accessibility
- Optimize performance or SEO

---

## 🔧 Prompt Formula for Frontend Code

```
Build a [component/page] using [React/Vue] and [CSS/Bootstrap/Tailwind].
It should do [behavior], have [props/data], and be responsive.
```

### ✅ Example

> Create a React dashboard card that shows the user's balance, recent transactions, and a transfer button. Use Bootstrap classes. Make it mobile-friendly.

---

## 🧱 Common Frontend Components

- `Header` / `Navbar`
- `Sidebar` / `Drawer`
- `DashboardCard`
- `TransactionList`
- `UserAvatar`
- `FormInput`
- `Modal`
- `ToastNotification`
- `Tabs` / `Accordion`

Prompt example:

```
Generate a responsive `TransactionList` component in React that shows date, amount, and description. Use Tailwind for styling.
```

---

## 🧠 State Management

Prompt:

> What's the best way to manage state in a React app with user profile, account balance, and transaction history?

AI might recommend:

- Context API for global state
- `useReducer` for complex state logic
- Libraries: Redux Toolkit, Zustand, Jotai

---

## 📱 Mobile Responsiveness

Prompt:

> Add responsiveness to this layout using CSS Grid or Bootstrap 5.

AI can suggest:

- Media queries
- Grid breakpoints
- Utility-first classes (Tailwind, Bootstrap)

---

## 🎨 Styling Techniques

AI can convert design specs to code:

- Figma-to-code descriptions
- Tailwind class suggestions
- Dark/light mode toggles
- SCSS structure prompts

Example:

```
Create a light/dark mode toggle button with Tailwind CSS and React hooks.
```

---

## 📦 Frontend Project Structure (React)

```
frontend/
├── src/
│   ├── components/
│   │   ├── ui/
│   │   ├── layout/
│   │   └── auth/
│   ├── pages/
│   ├── hooks/
│   ├── context/
│   ├── services/  # API logic
│   ├── App.jsx
│   └── index.js
├── public/
├── package.json
└── vite.config.js
```

---

## ✅ Frontend Linting and Testing Tools

- ESLint
- Prettier
- Stylelint (CSS/Tailwind)
- React Testing Library
- Playwright / Cypress (E2E)

Prompt:

> Write a test using React Testing Library for the LoginForm component that checks for email/password input and submit button.

---

## 📎 Frontend Integration Prompts

- **UI + API**:
  > Build a React form that submits user data to a FastAPI endpoint using Axios.

- **Validation**:
  > Use `yup` and `react-hook-form` to validate an account creation form.

- **Auth Flow**:
  > Build a protected route wrapper for React using JWTs stored in localStorage.

---

## 🧭 Up Next: Chapter 6 – Backend Development

Learn how to:

- Structure RESTful APIs with FastAPI
- Connect securely to Supabase
- Handle authentication, transactions, and role-based access

> 📂 File: [`06-backend.md`](./06-backend.md)
