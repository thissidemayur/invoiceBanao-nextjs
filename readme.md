# 📄 InvoiceBanao

<p align="center">
  <img src="./public/banner/invoicebanao-banner.svg" alt="InvoiceBanao Banner" width="800" />
</p>

[![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=nextdotjs)](https://nextjs.org/) [![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev/) [![Prisma](https://img.shields.io/badge/Prisma-6-2D3748?logo=prisma)](https://www.prisma.io/) [![NextAuth.js](https://img.shields.io/badge/NextAuth.js-v5--beta-000?logo=auth0)](https://authjs.dev/) [![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-4-38B2AC?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/) [![Mailtrap](https://img.shields.io/badge/Mailtrap-Email_Testing-28C8A7?logo=mailtrap)](https://mailtrap.io/) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](#-license) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#-contributing) [![Deploy](https://img.shields.io/badge/Deploy-Vercel-000?logo=vercel)](https://vercel.com/)

A full-stack **Next.js** application that allows users to **create, manage, and send invoices** directly to their clients' emails, along with transaction reports and dashboards.

Live Demo: **[invociebanao.thissidemayur.me](https://invoicebanao.thissidemayur.me/)**

---

## ✨ Features

- 🔐 **Cookie-based authentication** with NextAuth
- 🌐 **Magic Link Login**
- 📩 Send invoices and reminders via **Mailtrap SMTP & SDK**
- 🖨 Generate & send **PDF invoices from scratch (editable & copyable)**
- 📝 Create, edit, delete invoices
- ✅ Mark invoices as paid and send reminders
- 📊 Interactive **dashboard with graphs** (Recharts)
- 🔒 Protected routes & onboarding flow to collect user info
- ⚙️ Environment variable-based config
- 📬 PDF sent for both invoice creation and updates
- 🎨 Clean UI with Radix UI & Tailwind CSS

---

## 🧠 Tech Stack

**Frontend:**

- Next.js 15
- React 19
- Tailwind CSS 4
- Radix UI Components
- Recharts (Graphing)

**Backend:**

- Next.js API Routes
- NextAuth (cookie-based auth)
- Prisma ORM with PostgreSQL
- Mailtrap SMTP & SDK
- PDFKit, jsPDF, jsPDF-Autotable (for generating PDFs)

**Email & PDF**

- Mailtrap SMTP + SDK, Nodemailer
- PDFKit, jsPDF, jsPDF-Autotable

**Validation & Utils**

- Zod, date-fns, clsx, class-variance-authority

## Full `package.json` highlights are in the repo.

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/thissidemayur/invoiceBanao.git
cd invoiceBanao

```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Setup Environment Variables

```bash
AUTH_SECRET=
NEXTAUTH_URL=http://localhost:3000

FROM_EMAIL=
FROM_NAME=InvoiceBanao
APP_URL=


# This was inserted by `prisma init`:
DATABASE_URL=
#
NEXT_SERVER === NEXTAUTH_URL


RESEND_API_KEY=re_hGTbsQQv_BXjvnYdiRvpBHXqeDHDU1FTz

```

### 4️⃣ Run the App Locally

```bash
npm run dev
```

---

## 📦 API Endpoints (`/app/api/*`)

- `POST /api/auth/*` – Authentication ( Magic Link)
- `POST /api/invoices` – Create invoice, generate PDF, CRUD operations
- `POST /api/email` – Reminder emails & transactional messages
  `POST /api/signout` – logout account

> Your structure mentions `auth`, `email`, and `invoices`. Ensure proper HTTP verbs for CRUD: `GET/POST/PATCH/DELETE` as required.

---

## 🧭 Folder Structure (simplified)

```bash
app/
  api/
    auth/
    email/
    invoices/
    signOut/
  (routes...)  # app router pages, onboarding, dashboard, etc.
components/
lib/
prisma/
public/
  banner/
  screenshots/
```

---

## 🖼️ Screenshots

- ### Dashboard
- ### Create Invoice

## 🔗 Live Demo

```bash
👉 invoiceBanao.vercel.app
```

---

## 🙋 Author

**Mayur (thissidemayur)**

- GitHub: [@thissidemayur](https://github.com/thissidemayur)

---

## 🛠️ Contributing

Contributions are welcome!

1. Fork the repo
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit: `git commit -m "feat: add your feature"`
4. Push: `git push origin feat/your-feature`
5. Open a Pull Request

Please follow conventional commits and add tests where possible.

---
