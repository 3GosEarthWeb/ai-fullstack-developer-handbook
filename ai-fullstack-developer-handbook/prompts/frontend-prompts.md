# Frontend Prompts

This chapter includes practical AI prompts to generate React components, manage state, integrate APIs, test UIs, and scaffold full frontends using tools like GPT-4, Claude, or Copilot.

---

## ⚛️ React Component Prompts

**1. Basic Component Prompt**

```
Generate a React component called `UserCard` that displays a user’s name, avatar, and email. Use functional components.
```

**2. Form + Validation Prompt**

```
Create a React form with `react-hook-form` and `yup` for signing up a user with fields: fullName, email, password, confirmPassword.
```

**3. Reusable Input Prompt**

```
Write a reusable `TextInput` component that accepts props: label, name, value, onChange, error.
```

---

## 🔁 State & Hooks Prompts

**4. useEffect + Fetch Prompt**

```
Write a React component that fetches user data from `/api/profile` on mount using `useEffect` and `axios`.
```

**5. Custom Hook Prompt**

```
Create a custom hook `useAuth` that returns the current user and a logout function.
```

---

## 🔗 API Integration Prompts

**6. Supabase Prompt**

```
Generate a React hook that uses Supabase to fetch a list of transactions for the logged-in user.
```

**7. FastAPI Frontend Call**

```
Write a `useSubmitLoan` hook that sends a POST request to `/api/loans` with amount and term.
```

---

## 🎨 UI & Styling Prompts

**8. Tailwind UI Prompt**

```
Create a dashboard layout using Tailwind CSS with a sidebar, topbar, and main content area.
```

**9. Responsive Card Grid Prompt**

```
Generate responsive Tailwind classes for a grid of cards that adapts from 1 column on mobile to 4 columns on desktop.
```

---

## 🧪 Testing Prompts

**10. React Testing Library Prompt**

```
Write a test using React Testing Library for a `LoginForm` component that verifies form input and submit behavior.
```

**11. E2E Prompt with Playwright**

```
Generate an end-to-end Playwright test that logs in a user, visits the dashboard, and verifies the account balance appears.
```

---

## 🧠 AI Integration Prompts

**12. GPT Chat Prompt UI**

```
Create a React component for a chat UI that lets users send messages and see responses from an OpenAI-powered assistant.
```

**13. Prompt Builder UI**

```
Build a prompt builder form that lets users input an instruction and system context, then sends it to an LLM backend.
```

---

## 📦 Full Frontend Scaffold Prompt

**14. Dashboard Generator**

```
Generate a full frontend dashboard using React, React Router, and Tailwind with routes for /login, /dashboard, /settings, and /transactions.
```

**15. Auth Wrapper Prompt**

```
Create a ProtectedRoute wrapper in React that redirects unauthenticated users to the login page.
```

---

## ⚙️ Dev Prompts for Tooling

**16. Vite Config Prompt**

```
Create a `vite.config.js` for a React app using Tailwind CSS and aliases for `@components`, `@pages`, and `@utils`.
```

**17. Environment Setup Prompt**

```
Suggest .env file variables needed for connecting the frontend to Supabase and FastAPI.
```

---

## 💡 Bonus: Frontend Prompt Generator

```
Build a prompt-based UI that lets developers generate new components by describing them in natural language.
```

---

These prompts help you quickly scaffold, iterate, and polish UIs with AI. Pair them with GitHub Copilot or Claude for best results.

> Next: Use the [backend prompts](./backend-prompts.md) to complete your fullstack system.
