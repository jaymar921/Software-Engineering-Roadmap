# 🗺️ Software Engineering Roadmap

> A structured, beginner-friendly guide to becoming a job-ready software engineer — from writing your first line of code to deploying real-world applications with DevOps, security, and modern best practices.

Whether you're a complete beginner or switching careers, this roadmap walks you through every stage in the right order. Each section builds on the last, so follow the sequence and don't skip ahead.

---

## 📚 Table of Contents

1. [Fundamentals & Getting Started](#-1-fundamentals--getting-started)
2. [Choosing a Programming Language](#-2-choosing-a-programming-language)
3. [Version Control with GitHub](#-3-version-control-with-github)
4. [Build a Full-Stack Application](#-4-build-a-full-stack-application)
5. [Deploy Your Application (Free for Students)](#-5-deploy-your-application-free-for-students)
6. [CI/CD & Basic DevOps](#-6-cicd--basic-devops)
7. [DevSecOps & Containers (Docker)](#-7-devsecops--containers-docker)
8. [Build an E-Commerce App](#-8-build-an-e-commerce-app)

---

## 🧱 1. Fundamentals & Getting Started

Before picking a framework or building apps, you need to understand how computers, the web, and code actually work. These resources are considered the gold standard for beginners.

| Topic | Resource | Free? |
|---|---|---|
| Computer Science Basics | [Harvard CS50 (YouTube)](https://www.youtube.com/cs50) — watch Weeks 0–5 | ✅ |
| How the Web Works | [MDN Web Docs — How the Web Works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works) | ✅ |
| HTML & CSS | [MDN HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) | ✅ |
| Command Line | [The Missing Semester (MIT)](https://missing.csail.mit.edu/) | ✅ |
| Algorithms & Data Structures | [roadmap.sh — DSA Guide](https://roadmap.sh/datastructures-and-algorithms) | ✅ |
| Interactive Practice | [freeCodeCamp](https://www.freecodecamp.org/) | ✅ |
| Full Developer Roadmaps | [roadmap.sh](https://roadmap.sh/) | ✅ |

**Suggested learning order:**
1. CS50 Weeks 0–5 (how computers think)
2. MDN — How the Web Works
3. HTML & CSS basics
4. Command line basics
5. Data structures (arrays, linked lists, stacks, queues)

> 💡 **Tip:** Build a simple project as you go — a personal webpage or a to-do list. Learning by doing beats passive reading.

---

## 💻 2. Choosing a Programming Language

Choosing your first language can feel overwhelming. Here's what the data says about what's trending in 2026:

### 🔥 Trending Languages in 2026

| Language | Why Learn It | Best For |
|---|---|---|
| **Python** | #1 on TIOBE Index, dominant in AI/ML, biggest single-year jump in Stack Overflow survey | AI, data science, backend APIs |
| **JavaScript / TypeScript** | Used by 66% of developers (Stack Overflow 2025); TypeScript is now the #1 language on GitHub by contributor count | Web (frontend + backend), full-stack |
| **Rust** | Most admired language for 10 years running (72% admiration); growing fast in cloud infrastructure | Systems programming, performance-critical apps |
| **Go** | Simple syntax, built for concurrency and cloud-native tools | Backend services, microservices |
| **C#** | Strong in the Microsoft/.NET ecosystem, game development with Unity | Enterprise apps, game dev |

### 🎯 Recommendation for Beginners

**Start with JavaScript or Python.** Both have:
- Simple, readable syntax
- Massive communities and tutorials
- Immediate visual feedback (JS runs in the browser)
- Full-stack capability

Once comfortable, consider adding **TypeScript** (safer JS) for larger projects or **Python** for AI/ML work.

**Resources:**
- [JavaScript — The Odin Project](https://www.theodinproject.com/)
- [Python — Automate the Boring Stuff (Free Book)](https://automatetheboringstuff.com/)
- [TypeScript — Official Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [TIOBE Index (live rankings)](https://www.tiobe.com/tiobe-index/)
- [Stack Overflow Developer Survey 2025](https://survey.stackoverflow.co/2025/technology)

---

## 🐙 3. Version Control with GitHub

Git is non-negotiable. Every professional developer uses it daily. Learn this early.

### Core Concepts

- **Repository (repo)** — your project folder tracked by Git
- **Commit** — a saved snapshot of your changes
- **Branch** — a parallel version of your code for new features
- **Pull Request (PR)** — a request to merge your branch into main
- **Merge / Rebase** — combining branches

### Basic Git Commands

```bash
git init                    # Start a new repo
git clone <url>             # Copy a remote repo
git status                  # See what changed
git add .                   # Stage all changes
git commit -m "message"     # Save a snapshot
git push origin main        # Upload to GitHub
git pull                    # Get latest changes
git checkout -b feature/my-feature   # Create a new branch
git merge feature/my-feature         # Merge a branch
```

### Resources

| Resource | Link |
|---|---|
| Git basics (interactive) | [Learn Git Branching](https://learngitbranching.js.org/) |
| Free reference book | [Pro Git Book](https://git-scm.com/book/en/v2) |
| Quick fixes | [Oh Shit, Git!?!](https://ohshitgit.com/) |
| GitHub Docs | [docs.github.com](https://docs.github.com/en/get-started) |
| GitHub Skills (hands-on labs) | [skills.github.com](https://skills.github.com/) |

> 💡 **Good habits:** Write meaningful commit messages, use branches for every feature, and never commit directly to `main`.

---

## 🏗️ 4. Build a Full-Stack Application

A full-stack app has two parts working together:
- **Frontend** — what the user sees (HTML, CSS, JavaScript/React)
- **Backend** — the server, business logic, and database (Node.js, Python, etc.)

### Recommended Beginner Stack

```
Frontend:  React + Vite  (or plain HTML/CSS/JS)
Backend:   Node.js + Express  (or Python + Flask)
Database:  PostgreSQL  (or SQLite for local dev)
API:       REST  (JSON over HTTP)
```

### Project Structure Example (Node.js + React)

```
my-app/
├── client/          ← React frontend
│   ├── src/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
├── server/          ← Express backend
│   ├── routes/
│   ├── index.js
│   └── package.json
└── README.md
```

### Simple Backend (Express)

```js
// server/index.js
const express = require('express');
const app = express();
app.use(express.json());

app.get('/api/hello', (req, res) => {
  res.json({ message: 'Hello from the backend!' });
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

### Simple Frontend (React)

```jsx
// client/src/App.jsx
import { useEffect, useState } from 'react';

export default function App() {
  const [message, setMessage] = useState('');

  useEffect(() => {
    fetch('/api/hello')
      .then(res => res.json())
      .then(data => setMessage(data.message));
  }, []);

  return <h1>{message}</h1>;
}
```

### Resources

| Topic | Link |
|---|---|
| React Docs | [react.dev](https://react.dev/) |
| Node.js + Express | [expressjs.com](https://expressjs.com/) |
| Full-Stack Tutorial (The Odin Project) | [theodinproject.com](https://www.theodinproject.com/paths/full-stack-javascript) |
| REST API Guide | [roadmap.sh/api-design](https://roadmap.sh/api-design) |
| PostgreSQL Tutorial | [postgresqltutorial.com](https://www.postgresqltutorial.com/) |
| SQLZoo (interactive SQL) | [sqlzoo.net](https://sqlzoo.net/) |

---

## 🚀 5. Deploy Your Application (Free for Students)

Once your app works locally, it's time to put it on the internet. Here are the best free platforms for students:

### Platform Comparison

| Platform | Best For | Free Tier | Notes |
|---|---|---|---|
| [**Vercel**](https://vercel.com/) | Frontend / Next.js / static sites | ✅ Generous | Best DX for React/Next.js; global CDN included |
| [**Render**](https://render.com/) | Full-stack apps + databases | ✅ Static sites free; web services limited | Most beginner-friendly full-stack free tier in 2026 |
| [**Railway**](https://railway.app/) | Full-stack prototypes | ✅ $5 credit/month | Fast setup, great UI; had outages in 2025–2026 |
| [**Netlify**](https://www.netlify.com/) | Static sites / Jamstack | ✅ 100GB bandwidth | Great for frontend, no managed DB |
| [**Supabase**](https://supabase.com/) | Backend-as-a-service + PostgreSQL | ✅ Generous free DB | Excellent for adding auth + database quickly |
| [**GitHub Pages**](https://pages.github.com/) | Static HTML/CSS/JS sites | ✅ Completely free | No backend; great for portfolios |

### 🎓 GitHub Student Developer Pack

Students get free access to many paid tools including domains, cloud credits, and more:
👉 [education.github.com/pack](https://education.github.com/pack)

### Deploying to Vercel (Frontend)

```bash
npm install -g vercel
vercel login
vercel       # Follow prompts — done!
```

### Deploying to Render (Full-Stack)

1. Push your project to GitHub
2. Go to [render.com](https://render.com) → New → Web Service
3. Connect your GitHub repo
4. Set the build command (e.g. `npm install && npm run build`) and start command
5. Click Deploy — Render detects the runtime automatically

> 💡 **Recommendation for students:** Use **Vercel** for your frontend and **Render** or **Supabase** for your backend/database. Both are free, reliable, and beginner-friendly.

---

## ⚙️ 6. CI/CD & Basic DevOps

**CI/CD** stands for Continuous Integration / Continuous Deployment. It means every time you push code, automated tests run and your app can be automatically deployed — no manual steps needed.

### Why It Matters

- Catch bugs before they reach users
- Ship faster with confidence
- Simulate what real engineering teams do every day

### Key Concepts

| Term | Meaning |
|---|---|
| **CI (Continuous Integration)** | Automatically build and test code on every push |
| **CD (Continuous Deployment)** | Automatically deploy passing code to production |
| **Pipeline** | A series of automated steps (build → test → deploy) |
| **Workflow** | A configuration file that defines your pipeline |

### Example: GitHub Actions CI Workflow

Create `.github/workflows/ci.yml` in your repo:

```yaml
name: CI Pipeline

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build-and-test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Build project
        run: npm run build
```

### Example: Auto-Deploy to Render on Push

```yaml
name: Deploy to Render

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Trigger Render Deploy
        run: |
          curl -X POST ${{ secrets.RENDER_DEPLOY_HOOK_URL }}
```

> Set your Render deploy hook URL as a GitHub secret under `Settings → Secrets`.

### Resources

| Resource | Link |
|---|---|
| GitHub Actions Docs | [docs.github.com/actions](https://docs.github.com/en/actions) |
| GitHub Actions Quickstart | [Quickstart Guide](https://docs.github.com/en/actions/writing-workflows/quickstart) |
| roadmap.sh DevOps Guide | [roadmap.sh/devops](https://roadmap.sh/devops) |
| CI/CD Concepts (freeCodeCamp) | [freecodecamp.org](https://www.freecodecamp.org/news/what-is-ci-cd/) |

---

## 🔒 7. DevSecOps & Containers (Docker)

**DevSecOps** means baking security into your development process from day one — not as an afterthought. **Docker** lets you package your app and all its dependencies into a portable container that runs the same everywhere.

### Basic Security Practices

- Never commit secrets (API keys, passwords) to Git — use `.env` files and add them to `.gitignore`
- Validate all user input on the backend to prevent SQL Injection and XSS attacks
- Use HTTPS everywhere (Vercel and Render do this for free)
- Keep dependencies updated (`npm audit`, `pip check`)
- Use environment variables for all sensitive configuration

### Docker Basics

Docker packages your app into a **container** — a lightweight, isolated environment. This means "it works on my machine" becomes "it works everywhere."

```
your code + runtime + dependencies = Docker Image → runs as a Container
```

**Basic Dockerfile (Node.js app):**

```dockerfile
# Use official Node.js base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy dependency files
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the app
COPY . .

# Expose the port
EXPOSE 3000

# Start the app
CMD ["node", "server/index.js"]
```

**Common Docker Commands:**

```bash
docker build -t my-app .          # Build an image
docker run -p 3000:3000 my-app    # Run the container
docker ps                         # List running containers
docker stop <container_id>        # Stop a container
docker-compose up                 # Start multi-container apps
```

**Docker Compose (frontend + backend + database together):**

```yaml
# docker-compose.yml
version: '3.8'
services:
  backend:
    build: ./server
    ports:
      - "3000:3000"
    environment:
      - DATABASE_URL=postgres://user:pass@db:5432/mydb
    depends_on:
      - db

  frontend:
    build: ./client
    ports:
      - "5173:5173"

  db:
    image: postgres:16
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
      POSTGRES_DB: mydb
```

### Resources

| Resource | Link |
|---|---|
| Docker Getting Started | [docs.docker.com/get-started](https://docs.docker.com/get-started/) |
| Docker in 100 Seconds (Fireship) | [YouTube](https://www.youtube.com/watch?v=Gjnup-PuquQ) |
| OWASP Top 10 (Security Risks) | [owasp.org/Top10](https://owasp.org/www-project-top-ten/) |
| GitHub Secret Scanning | [docs.github.com/secret-scanning](https://docs.github.com/en/code-security/secret-scanning/introduction/about-secret-scanning) |
| roadmap.sh Docker Guide | [roadmap.sh/docker](https://roadmap.sh/docker) |

---

## 🛒 8. Build an E-Commerce App

An e-commerce app ties together everything in this roadmap: frontend UI, backend APIs, a database, authentication, payments, and deployment. It's one of the best capstone projects to put on your portfolio.

### Core Features to Build

- 🛍️ Product listing page with search and filters
- 🛒 Shopping cart (add/remove/update items)
- 🔐 User authentication (register, login, JWT or sessions)
- 💳 Checkout with payment integration (Stripe)
- 📦 Order history and management
- 🔑 Admin panel (add/edit/delete products)

### Recommended Tech Stack

```
Frontend:    React + Tailwind CSS
Backend:     Node.js + Express  (or Next.js full-stack)
Database:    PostgreSQL + Prisma ORM
Auth:        JWT  (or NextAuth.js)
Payments:    Stripe API
Deployment:  Vercel (frontend) + Render (backend + DB)
```

### Basic Product API Example

```js
// GET /api/products
app.get('/api/products', async (req, res) => {
  const products = await prisma.product.findMany();
  res.json(products);
});

// POST /api/cart
app.post('/api/cart', authenticate, async (req, res) => {
  const { productId, quantity } = req.body;
  const item = await prisma.cartItem.create({
    data: { productId, quantity, userId: req.user.id }
  });
  res.json(item);
});
```

### Open Source Examples & References

| Project | Link | Notes |
|---|---|---|
| **Medusa.js** | [medusajs.com](https://medusajs.com/) | Open-source e-commerce engine, great to study |
| **Vendure** | [vendure.io](https://vendure.io/) | TypeScript e-commerce framework |
| **Next.js Commerce** | [vercel.com/templates/next.js/nextjs-commerce](https://vercel.com/templates/next.js/nextjs-commerce) | Official Vercel e-commerce starter |
| **Stripe Docs** | [stripe.com/docs](https://stripe.com/docs) | Payment integration guide |
| **Full Tutorial (freeCodeCamp)** | [freeCodeCamp E-Commerce](https://www.freecodecamp.org/news/build-a-full-stack-application-with-nextjs/) | Step-by-step full-stack app |

> 💡 **Start small.** Build a product listing + cart first. Add auth next. Add payments last. Ship it to Vercel/Render as early as possible.

---

## 📌 Quick Reference — Tools & Links

| Category | Tool | Link |
|---|---|---|
| Roadmaps | roadmap.sh | [roadmap.sh](https://roadmap.sh) |
| CS Fundamentals | Harvard CS50 | [cs50.harvard.edu](https://cs50.harvard.edu/x/) |
| Practice Coding | LeetCode | [leetcode.com](https://leetcode.com) |
| Practice Coding | Codecademy | [codecademy.com](https://www.codecademy.com/) |
| Web Reference | MDN Web Docs | [developer.mozilla.org](https://developer.mozilla.org/) |
| Git Learning | Learn Git Branching | [learngitbranching.js.org](https://learngitbranching.js.org/) |
| Deployment | Vercel | [vercel.com](https://vercel.com) |
| Deployment | Render | [render.com](https://render.com) |
| Database | Supabase | [supabase.com](https://supabase.com) |
| Containers | Docker | [docker.com](https://www.docker.com/) |
| Payments | Stripe | [stripe.com](https://stripe.com) |
| CI/CD | GitHub Actions | [github.com/features/actions](https://github.com/features/actions) |
| Security | OWASP Top 10 | [owasp.org](https://owasp.org/www-project-top-ten/) |

---

## 🏷️ Tags

`#software-engineering` `#beginner` `#roadmap` `#programming` `#javascript` `#python` `#typescript` `#webdevelopment` `#fullstack` `#backend` `#frontend` `#react` `#nodejs` `#docker` `#devops` `#cicd` `#github-actions` `#devsecops` `#deployment` `#vercel` `#render` `#ecommerce` `#student` `#learning` `#career` `#open-source`

---

<p align="center">
  Made for students, by developers who've been there. ⭐ Star this repo if it helped you!
</p>
