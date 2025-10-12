# 🌟 Personal Portfolio & Blog Project

A modern, responsive **personal portfolio website** built with **Next.js**, featuring a landing page, blog functionality, and detailed project showcase. The project also includes a secure **admin panel**, rate-limiting, and enhanced middleware security.

---

## 🛠️ Features

### **Frontend**
- **Landing Page** – Fully responsive design showcasing personal information and skills.
- **Projects Section** – Display projects with descriptions, tech stack, and links.
- **Blog Section** – Add and manage blogs easily with markdown support.
- **Admin Dashboard** – Manage blogs, projects, and analytics.

### **Backend / Middleware**
- **Rate Limiting** – Protects against abuse by limiting requests per IP (`10,000 requests per minute`).
- **Protected Routes** – Admin paths (`/admin`, `/admin/dashboard`, `/admin/blogs`, `/admin/analytics`) are secured.
- **Public Routes** – Landing page and login paths are publicly accessible.
- **Security Headers** – Includes:
  - `Content-Security-Policy` with nonce for scripts/styles
  - `X-DNS-Prefetch-Control`
  - `Strict-Transport-Security`
  - `X-XSS-Protection`
  - `X-Frame-Options`
  - `X-Content-Type-Options`
  - `Referrer-Policy`
  - `Permissions-Policy`
- **IP Detection** – Supports `x-forwarded-for` and `x-real-ip` headers for accurate client IP tracking.
- **Middleware** – Handles redirection to `/auth/login` for protected paths.

### **Integration**
- **Upstash Redis** – For rate-limiting and request tracking.
- **Appwrite** – Optional integration for backend services (authentication, database, storage).

---

## 🗂️ Project Structure (Key Files)

| File | Purpose |
|------|---------|
| `content.ts` | Landing page & blog content configuration |
| `appwrite.ts` | Appwrite integration & project changes |
| `constant.ts` | Common constants for the project |
| `gsap.ts` | GSAP animations for interactive UI |
| `motion.ts` | Motion configuration for animations |
| `publicApiAuth.ts` | Public API authentication helpers |
| `sanitier.ts` | Input sanitization & validation |
| `testsitemap.ts` | Sitemap testing and generation |
| `middleware.ts` | Security, rate-limiting, and protected route handling |

---

## ⚡ Tech Stack
- **Frontend:** Next.js, React, Tailwind CSS, GSAP  
- **Backend:** Node.js, Appwrite (optional)  
- **Database:** Appwrite DB / MongoDB  
- **Cache/Rate Limiting:** Upstash Redis  
- **Security:** Middleware with CSP, secure headers, and route protection  

---

## 🚀 Getting Started

### **1. Clone the repository**
```bash
git clone https://github.com/amarkumar55/your-portfolio.git
cd your-portfolio
