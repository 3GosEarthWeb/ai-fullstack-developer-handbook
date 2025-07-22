# Chapter 12: Admin & Analytics

## 🧑‍💼 Why Admin Panels Matter

Admin dashboards are essential for:

- Managing users, content, and roles
- Monitoring transactions or logs
- Approving actions (e.g. loans, posts)
- Gaining insight into system performance or user behavior

---

## 📊 Analytics Dashboards

Analytics let you:

- Track KPIs in real time
- Visualize trends over time
- Detect anomalies (e.g., drop in signups)
- Improve product decisions with data

---

## 🧠 How AI Helps

- Generate full admin panel code from schema
- Auto-generate dashboard widgets based on table structure
- Suggest the best chart type based on your data
- Create SQL queries for charts and filters
- Analyze user behavior patterns

---

## 🧪 Prompt Templates

```
Build an admin panel in [framework] with [features] and [role-based access].
```

```
Create a dashboard that shows [metrics] using [chart types] from [data source].
```

✅ Example:

> Build a React + Supabase admin dashboard with tabs for users, loans, and audit logs. Add a bar chart for weekly loan approvals.

---

## ⚙️ Tech Stack Options

| Feature         | Tools                                |
|-----------------|--------------------------------------|
| UI Framework    | React, Next.js, Vue, Django Admin    |
| Charts          | Recharts, Chart.js, ECharts, Plotly  |
| Backend Auth    | Supabase, Firebase, FastAPI, Django  |
| Access Control  | RBAC, Supabase policies, OAuth       |
| AI Enhancements | LangChain, GPT-4, Retool AI          |

---

## ⚒️ Admin Page Example (React + Supabase)

```tsx
import { useEffect, useState } from 'react'
import { supabase } from '../lib/supabase'

function UsersTable() {
  const [users, setUsers] = useState([])

  useEffect(() => {
    supabase.from('users').select('*').then(({ data }) => setUsers(data))
  }, [])

  return (
    <table>
      <thead><tr><th>Email</th><th>Role</th></tr></thead>
      <tbody>
        {users.map(user => (
          <tr key={user.id}><td>{user.email}</td><td>{user.role}</td></tr>
        ))}
      </tbody>
    </table>
  )
}
```

Prompt:

> Generate a React table to list all users from the Supabase `users` table with pagination and search.

---

## 📉 Chart Example (Recharts)

```tsx
<BarChart width={600} height={300} data={loanStats}>
  <XAxis dataKey="week" />
  <YAxis />
  <Tooltip />
  <Bar dataKey="approved" fill="#82ca9d" />
</BarChart>
```

Prompt:

> Create a bar chart to show the number of loan approvals per week.

---

## 🔒 Admin Security Best Practices

- ✅ Role-based access (RBAC)
- ✅ Audit logs for all actions
- ✅ Prevent exposure of user PII
- ✅ Admin API endpoints require elevated auth
- ✅ Use environment variables for credentials

Prompt:

> Create Supabase policies to allow only admin role to update or delete users.

---

## 📈 Metrics to Track in Dashboards

- 🧑‍💼 Active Users
- 💳 Transactions Processed
- ⏱️ Response Times
- 🐛 Error Rates
- 💸 Revenue or Payments
- 🔐 Login Failures

Prompt:

> Show me 5 key metrics for a fintech dashboard with Supabase + FastAPI backend.

---

## 🧭 Up Next: Chapter 13 – Continuous Integration (CI/CD)

Now that your app is built and managed, we’ll explore how to:

- Automatically test every pull request
- Deploy to Vercel, Netlify, or Render
- Automate checks using AI agents and GitHub Actions

> 📂 File: [`13-ci-cd.md`](./13-ci-cd.md)
