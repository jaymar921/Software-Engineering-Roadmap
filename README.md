# 🗺️ Software Engineering Roadmap

> A step by step path for people who have never written a line of code before, all the way to shipping real applications.

If you've never programmed before, welcome. This roadmap is built for you specifically. It's broken into phases, and each phase has one job: get you ready for the next one. You are not expected to understand everything on your first pass, and that's normal. Every engineer started exactly where you are now.

---

## 🚦 How to Use This Roadmap

A few ground rules before you start, these matter more than they sound like they do:

1. **Go in order.** Phase 2 assumes you finished Phase 1. Skipping ahead usually means backtracking later, which is more frustrating than just going slow now.
2. **Don't try to learn everything at once.** You do not need to know Docker, CI/CD, or security best practices to write your first program. Those come later, on purpose.
3. **This takes time.** Realistically, 6 to 12 months of consistent practice (a few hours a week) to go from zero to your first working full-stack app. That is completely normal.
4. **Build small things constantly.** Reading and watching tutorials feels productive but doesn't build skill by itself. Typing code, breaking it, and fixing it does.
5. **Getting stuck is part of the process, not a sign you're bad at this.** Every developer, including senior ones, spends a huge chunk of their time confused and Googling errors.

**The phases:**

| Phase | What you'll do | You'll know you're ready to move on when... |
|---|---|---|
| 0 | Get oriented, set up your tools | You have a code editor open and you understand a few basic terms |
| 1 | Learn programming fundamentals | You can write a program with variables, loops, and conditionals without copy-pasting |
| 2 | Pick and practice your first language | You're comfortable writing small programs from scratch |
| 3 | Learn Git and GitHub | You can save and upload your code changes without panicking |
| 4 | Build your first full-stack app | You have something running on your own computer that a frontend talks to a backend |
| 5 | Put it on the internet | A stranger can visit a link and use your app |
| 6 | Learn intermediate practices (CI/CD, Docker, security) | Optional, come back after a few projects |
| 7 | Build a capstone project | You have something substantial for a portfolio |

---

## 🧠 Phase 0: Before You Write Any Code

### What is "programming," really?

Programming is giving a computer a precise list of instructions, written in a language it can understand, to make it do something. That's it. Everything else (languages, frameworks, frameworks-on-top-of-frameworks) is just tooling built on top of that basic idea.

### A few words you'll see constantly (bookmark this)

| Term | Plain English meaning |
|---|---|
| **IDE / Code Editor** | The app you write code in. You'll use [VS Code](https://code.visualstudio.com/), it's free. |
| **Terminal / Command line** | A text-based way to give your computer commands, instead of clicking buttons |
| **Repository (repo)** | A folder for your project that Git keeps a history of |
| **Framework** | A pre-built toolkit that handles the boring, repetitive parts so you don't rebuild them every time |
| **Library** | Similar to a framework, but you use pieces of it as needed instead of building your whole app around it |
| **API** | A way for two pieces of software to talk to each other (like a waiter taking your order to the kitchen) |
| **Frontend** | The part of an app the user sees and clicks on |
| **Backend** | The part of an app that runs behind the scenes (logic, database access) |
| **Database** | Where an app's data is permanently stored |
| **Deployment** | Putting your app on a server so anyone on the internet can use it |
| **Package manager** | A tool that installs and manages the external code libraries your project depends on (like `npm` for JavaScript) |

You don't need to memorize this table. Just come back to it whenever a term feels unfamiliar.

### Set up your tools

1. Install [VS Code](https://code.visualstudio.com/) (your code editor)
2. Install a modern browser (Chrome or Firefox, either is fine)
3. Create a free [GitHub account](https://github.com/) (you'll need this in Phase 3)

### A tiny confidence-building exercise

Before diving into a full course, do this:

1. Create a file called `index.html`
2. Paste this in:
   ```html
   <!DOCTYPE html>
   <html>
     <body>
       <h1>Hello, world!</h1>
     </body>
   </html>
   ```
3. Open it in your browser (double-click the file)

You just wrote and ran code. That's the whole loop you'll be repeating for the rest of your career: write code, run it, see what happens, adjust.

---

## 🧱 Phase 1: Programming Fundamentals

This phase teaches you *how to think like a programmer*, separate from any specific language. Concepts like loops, variables, and conditionals work almost the same across every language, so what you learn here transfers everywhere.

**Pick ONE primary path below.** Don't try to do both, that's a common beginner trap that just slows you down.

| If you prefer... | Go with |
|---|---|
| Structured video lectures, like a real university course | [Harvard CS50 (YouTube)](https://www.youtube.com/cs50) — watch weeks 0 through 5 |
| Hands-on, interactive, learn-by-typing-code | [freeCodeCamp](https://www.freecodecamp.org/) |

**What you're aiming to understand by the end of this phase:**
- Variables (storing a value under a name)
- Conditionals (`if` / `else`, making decisions)
- Loops (`for` / `while`, repeating actions)
- Functions (reusable blocks of code)
- Basic data structures (lists/arrays, key-value pairs)

**Optional, only if you're curious about how the web works underneath:**
- [MDN — How the Web Works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)
- [The Missing Semester (MIT)](https://missing.csail.mit.edu/) — command line basics

✅ **Checkpoint:** You can write a small program from scratch (not copy-pasted) that takes some input, makes a decision with it, and loops over something. If you can do that without following a tutorial line by line, move on.

---

## 💻 Phase 2: Pick Your First Language

Here's the honest, no-jargon version: for a first language, it barely matters which one you pick, since the core concepts are the same. What matters is picking one and sticking with it long enough to get good.

**Recommended for beginners:**

| Language | Why it's a solid first choice |
|---|---|
| **JavaScript** | Runs directly in your browser, no setup needed, instant visual feedback. Also usable for both frontend and backend later. |
| **Python** | Very readable syntax, close to plain English, huge beginner community |

If you're not sure, pick **JavaScript**. The instant feedback (see your code change a webpage live) tends to keep beginners motivated longer than a lot of alternatives.

> Curious about other languages like C#, Rust, or Go? They're great, but better picked up *after* your first language, once you already understand core programming concepts. See the [Appendix](#-appendix) for a fuller comparison.

**Resources:**
- [JavaScript — The Odin Project](https://www.theodinproject.com/)
- [Python — Automate the Boring Stuff (free book)](https://automatetheboringstuff.com/)

✅ **Checkpoint:** You're comfortable writing small standalone programs (a calculator, a to-do list that only works in the console, a simple game) in your chosen language without heavy hand-holding.

---

## 📁 Phase 3: Learn Git and GitHub

### Why this matters before you build anything bigger

Imagine writing an essay with no undo button and no way to save different drafts. That's coding without Git. Git is a tool that saves snapshots of your code over time, so you can always go back, and GitHub is a website that hosts those snapshots online so you can share your work (and so employers can see it).

### Core concepts, explained plainly

- **Repository (repo):** the project folder Git is tracking
- **Commit:** a saved snapshot of your changes, with a short note describing what changed
- **Branch:** a separate copy of your code where you can experiment without touching the main version
- **Pull Request (PR):** a request to merge your branch's changes into the main version
- **Push / Pull:** uploading your commits to GitHub / downloading someone else's commits

### The only commands you actually need at this stage

```bash
git init                    # Start tracking a folder with Git
git status                  # See what's changed since your last commit
git add .                   # Stage all your changes to be committed
git commit -m "message"     # Save a snapshot, with a short description
git push origin main        # Upload your snapshots to GitHub
git pull                    # Download the latest changes from GitHub
```

Everything else (rebasing, resolving merge conflicts, cherry-picking) can wait. Learn those when you actually run into a situation that needs them, not before.

**Resources:**
- [Learn Git Branching (interactive, highly recommended)](https://learngitbranching.js.org/)
- [Oh Shit, Git!?! (for when you mess up, and you will)](https://ohshitgit.com/)

✅ **Checkpoint:** You can create a repo, make changes, commit them, and push them to GitHub without needing to look up every step.

---

## 🏗️ Phase 4: Build Your First Full-Stack Application

### Frontend vs backend, in plain terms

Think of a restaurant. The **frontend** is the dining area: the menu, the tables, what the customer sees and interacts with. The **backend** is the kitchen: it's where the actual work happens, out of sight, and it sends the finished result back out front.

A **full-stack app** just means you're building both sides and connecting them.

### Recommended beginner stack

```
Frontend:  React + Vite   (or plain HTML/CSS/JS if you want fewer moving parts first)
Backend:   Node.js + Express
Database:  SQLite for local practice, PostgreSQL once you're comfortable
API style: REST (your frontend and backend send each other JSON, a simple text format for data)
```

### Project structure

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

### A minimal backend

```js
// server/index.js
const express = require('express');
const app = express();
app.use(express.json());

// This creates one "endpoint," a URL the frontend can request data from
app.get('/api/hello', (req, res) => {
  res.json({ message: 'Hello from the backend!' });
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

### A minimal frontend that talks to it

```jsx
// client/src/App.jsx
import { useEffect, useState } from 'react';

export default function App() {
  const [message, setMessage] = useState('');

  useEffect(() => {
    // Ask the backend for data as soon as the page loads
    fetch('/api/hello')
      .then(res => res.json())
      .then(data => setMessage(data.message));
  }, []);

  return <h1>{message}</h1>;
}
```

What's happening here: the frontend asks the backend for data at `/api/hello`, the backend responds with a small piece of JSON, and the frontend displays it on the page. Every full-stack app, no matter how complex, is some version of this loop repeated many times over.

**Resources:**
- [React Docs](https://react.dev/)
- [Express Docs](https://expressjs.com/)
- [Full-Stack Tutorial (The Odin Project)](https://www.theodinproject.com/paths/full-stack-javascript)

> If this phase feels genuinely hard, that's expected, it's usually the biggest jump in the whole roadmap. Take it slow, build something tiny (even a single button that fetches one piece of data) before adding more.

✅ **Checkpoint:** You have a frontend and backend running at the same time on your computer, and the frontend successfully displays data it got from the backend.

---

## 🚀 Phase 5: Put Your App on the Internet

Right now your app only works on your own computer. Deployment means putting it somewhere anyone with a link can use it.

**The simplest path for beginners:**

- **Frontend →** [Vercel](https://vercel.com/) (free, best experience for React apps)
- **Backend + database →** [Render](https://render.com/) (free tier, beginner-friendly)

### Deploying your frontend to Vercel

```bash
npm install -g vercel
vercel login
vercel       # follow the prompts, it handles the rest
```

### Deploying your backend to Render

1. Push your project to GitHub (you already know how, from Phase 3)
2. Go to [render.com](https://render.com) → New → Web Service
3. Connect your GitHub repo
4. Set your build command (e.g. `npm install && npm run build`) and start command
5. Click Deploy, Render figures out the rest

### 🎓 If you're a student

GitHub gives students free access to a bunch of paid developer tools, domains, and cloud credits: [education.github.com/pack](https://education.github.com/pack)

✅ **Checkpoint:** You can send someone a link, and they can open and use your app without needing your computer running.

---

## ⚙️ Phase 6: Level Up (Intermediate Practices)

> **Come back to this phase after you've built and deployed 2 to 3 small projects.** Everything below is genuinely useful, but it solves problems you haven't run into yet. Learning it too early tends to just feel like noise.

### CI/CD (Continuous Integration / Continuous Deployment)

The idea: every time you push code, tests run automatically, and if they pass, your app deploys automatically. No manual steps.

**Why it matters:** it catches bugs before real users see them, and it mirrors how real engineering teams actually work.

| Term | Meaning |
|---|---|
| **CI** | Automatically build and test your code every time you push |
| **CD** | Automatically deploy code that passes its tests |
| **Pipeline** | The sequence of automated steps: build, test, deploy |
| **Workflow** | A config file that defines your pipeline |

**Example GitHub Actions CI workflow** (`.github/workflows/ci.yml`):

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

**Auto-deploy to Render on push:**

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

(Set your Render deploy hook URL as a GitHub secret under `Settings → Secrets`.)

**Resources:**
- [GitHub Actions Quickstart](https://docs.github.com/en/actions/writing-workflows/quickstart)
- [CI/CD Concepts (freeCodeCamp)](https://www.freecodecamp.org/news/what-is-ci-cd/)

### Basic security habits (DevSecOps)

- Never commit secrets (API keys, passwords) to Git, use `.env` files and add them to `.gitignore`
- Validate all user input on the backend, this is what prevents SQL injection and XSS attacks
- Use HTTPS everywhere (Vercel and Render already do this for free)
- Keep dependencies updated (`npm audit`)
- Store sensitive configuration in environment variables, never hardcoded

**Resource:** [OWASP Top 10](https://owasp.org/www-project-top-ten/) (the most common security risks, worth skimming once)

### Docker

Docker packages your app plus everything it needs to run into a portable container, so "it works on my machine" becomes "it works everywhere."

```
your code + runtime + dependencies = Docker Image → runs as a Container
```

**Basic Dockerfile (Node.js app):**

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install --production
COPY . .
EXPOSE 3000
CMD ["node", "server/index.js"]
```

**Common commands:**

```bash
docker build -t my-app .          # Build an image
docker run -p 3000:3000 my-app    # Run the container
docker ps                         # List running containers
docker stop <container_id>        # Stop a container
docker-compose up                 # Start multi-container apps
```

**Docker Compose (frontend + backend + database together):**

```yaml
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

**Resources:**
- [Docker Getting Started](https://docs.docker.com/get-started/)
- [Docker in 100 Seconds (Fireship, YouTube)](https://www.youtube.com/watch?v=Gjnup-PuquQ)

✅ **Checkpoint for this whole phase:** You understand *why* each of these tools exists, even if you're not fluent in all of them yet. That's enough to move on.

---

## 🛒 Phase 7: Capstone Project (E-Commerce App)

This ties together everything above: frontend UI, a backend API, a database, authentication, payments, and deployment. It's one of the strongest portfolio projects you can build.

### Core features to build, in this order

1. 🛍️ Product listing page with search and filters
2. 🛒 Shopping cart (add, remove, update quantity)
3. 🔐 User authentication (register, login, sessions or JWT)
4. 💳 Checkout with Stripe payment integration
5. 📦 Order history
6. 🔑 Admin panel to add/edit/delete products

**Recommended tech stack:**

```
Frontend:    React + Tailwind CSS
Backend:     Node.js + Express (or Next.js full-stack)
Database:    PostgreSQL + Prisma ORM
Auth:        JWT (or NextAuth.js)
Payments:    Stripe API
Deployment:  Vercel (frontend) + Render (backend + DB)
```

**A small taste of what the backend looks like:**

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

**Real open-source projects worth studying (not copying):**

| Project | Link | Notes |
|---|---|---|
| Medusa.js | [medusajs.com](https://medusajs.com/) | Open-source e-commerce engine |
| Vendure | [vendure.io](https://vendure.io/) | TypeScript e-commerce framework |
| Next.js Commerce | [vercel.com/templates](https://vercel.com/templates/next.js/nextjs-commerce) | Official Vercel starter |
| Stripe Docs | [stripe.com/docs](https://stripe.com/docs) | Payment integration guide |

> 💡 Build in order: product listing and cart first, then auth, then payments last. Deploy early and often, don't wait until it's "finished" to put it online.

---

## 📎 Appendix

### Fuller language comparison (for the curious)

| Language | Notable strengths | Best used for |
|---|---|---|
| **Python** | Extremely popular in AI/ML and data science, very readable | AI, data science, backend APIs |
| **JavaScript / TypeScript** | Used by the majority of developers, runs in every browser | Web apps, both frontend and backend |
| **Rust** | Consistently rated one of the most-liked languages, strong performance | Systems programming, performance-critical software |
| **Go** | Simple syntax, designed for concurrency | Backend services, cloud infrastructure |
| **C#** | Deep integration with the Microsoft/.NET ecosystem, strong in game dev via Unity | Enterprise applications, game development |

None of these are "wrong" first languages. They're just better picked up after you already have fundamentals under your belt, so you can evaluate them on their own merits instead of fighting core programming concepts and new syntax at the same time.

### Fuller deployment platform comparison

| Platform | Best for | Free tier | Notes |
|---|---|---|---|
| [Vercel](https://vercel.com/) | Frontend / Next.js / static sites | ✅ Generous | Best experience for React/Next.js, global CDN included |
| [Render](https://render.com/) | Full-stack apps + databases | ✅ Static sites free, web services limited | Most beginner-friendly full-stack free tier |
| [Railway](https://railway.app/) | Full-stack prototypes | ✅ $5 credit/month | Fast setup, has had occasional outages |
| [Netlify](https://www.netlify.com/) | Static sites / Jamstack | ✅ 100GB bandwidth | No managed database |
| [Supabase](https://supabase.com/) | Backend-as-a-service + PostgreSQL | ✅ Generous free DB | Great for adding auth and a database quickly |
| [GitHub Pages](https://pages.github.com/) | Static HTML/CSS/JS sites | ✅ Completely free | No backend, good for portfolios |

### Quick reference links

| Category | Tool | Link |
|---|---|---|
| Roadmaps | roadmap.sh | [roadmap.sh](https://roadmap.sh) |
| CS Fundamentals | Harvard CS50 | [cs50.harvard.edu](https://cs50.harvard.edu/x/) |
| Practice Coding | LeetCode | [leetcode.com](https://leetcode.com) |
| Practice Coding | Codecademy | [codecademy.com](https://www.codecademy.com/) |
| Web Reference | MDN Web Docs | [developer.mozilla.org](https://developer.mozilla.org/) |
| Git Learning | Learn Git Branching | [learngitbranching.js.org](https://learngitbranching.js.org/) |
| Database Practice | SQLZoo | [sqlzoo.net](https://sqlzoo.net/) |
| Security | OWASP Top 10 | [owasp.org](https://owasp.org/www-project-top-ten/) |

---

## 🏷️ Tags

`#software-engineering` `#beginner` `#roadmap` `#programming` `#javascript` `#python` `#typescript` `#webdevelopment` `#fullstack` `#backend` `#frontend` `#react` `#nodejs` `#docker` `#devops` `#cicd` `#github-actions` `#devsecops` `#deployment` `#vercel` `#render` `#ecommerce` `#student` `#learning` `#career` `#open-source`

---

<p align="center">
  Made for students, by developers who've been there. If you're stuck, that means you're doing it right. ⭐ Star this repo if it helped you!
</p>
