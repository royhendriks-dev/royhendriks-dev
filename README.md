<div align="center">

# Hi, I'm Roy Hendriks 👋

### Full Stack Software Developer · Angular · TypeScript · Java · Quarkus

I build web applications end to end, host them on my own Kubernetes cluster at home, and experiment with AI agents and developer tooling.

*🇳🇱 Ik ben fullstack developer en bouw, host en automatiseer mijn eigen projecten, van Angular-frontend tot Kubernetes op een MacBook in de woonkamer.*

[![Website](https://img.shields.io/badge/royhendriks.com-0D1117?style=for-the-badge&logo=googlechrome&logoColor=58A6FF)](https://royhendriks.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0D1117?style=for-the-badge&logo=linkedin&logoColor=0A66C2)](https://www.linkedin.com/in/roy-hendriks-dev/)
[![GitHub](https://img.shields.io/badge/GitHub-0D1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/royhendriks-dev)

</div>

---

## 🧰 Tech stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=angular,typescript,javascript,java,nodejs,html,css,postgres,docker,kubernetes,githubactions,cloudflare,grafana,git,github&theme=dark" alt="Technology icons" />
</p>

| Area | Technologies |
|---|---|
| **Frontend** | Angular 22, TypeScript, SCSS, Vitest |
| **Backend** | Java 25, Quarkus 3 (LTS), REST APIs, PostgreSQL 18, Flyway |
| **DevOps** | Docker (multi-arch amd64 + arm64), Kubernetes (k3s), GitHub Actions, GHCR, Cloudflare Tunnel |
| **Quality** | SonarQube Cloud, 80% coverage gates, WCAG 2.2 AA, OWASP-based security review |
| **Observability** | Structured JSON logs, Loki, Grafana, Alloy |
| **Exploring** | AI agents, local LLMs, agentic development workflows |

---

## 🚀 Featured projects

### 🖥️ RoyHendriks.DevOS93 — my portfolio as a retro desktop
**[royhendriks.com](https://royhendriks.com)** · *Angular 22 · Quarkus · PostgreSQL · k3s*

My portfolio is a clickable **Windows 98-style desktop** with draggable windows, a taskbar and a Start menu. It is a full-stack showcase, not just a static page:

- 🌍 **Bilingual (NL/EN):** all text is served by the backend and a test guards that both languages have the same keys.
- 🎮 **Games with their own top 10 in the database:** Snake, Oilcap Pro (my own take on the 90s pipe game), Pong and Breakout 98 (15 levels), plus Paint and an exact-decimal calculator. A name filter masks profanity in highscores.
- 🔐 **Private admin area:** Argon2id password hashes, `HttpOnly` session cookies, CSRF protection, lockout after failed attempts, CSP with nonce, and a review against OWASP ASVS / Top 10.
- 📱 **Works on phones** and is built to **WCAG 2.2 AA** (checked with axe-core).
- 🔢 **Privacy-friendly analytics:** an anonymous visitor counter in my own backend. No cookies, no IP addresses.
- 🧩 **Apps inside the desktop:** the *Projects* folder launches microservices like the recipes app in an iframe after a terminal-style boot animation.

> The repository is private. The live site is the best way to see it.

### 🍳 recipes-for-me — a recipe microservice
**[royhendriks-dev/recipes-for-me](https://github.com/royhendriks-dev/recipes-for-me)** · *Angular · TypeScript · nginx*

A mobile-first recipe app that runs as its own pod behind the portfolio.

- 52 recipes in Dutch and English, served by the portfolio backend
- Servings slider (2 / 4), tick-off ingredient lists, kitchen timers, favorites
- **Share a recipe to your own Discord channel** through a server-side OAuth2 webhook relay (no login, no webhook in the browser)
- Own CI/CD: tests with 80% coverage gate, SonarQube Cloud, multi-arch images on GHCR, a manual release workflow

### 🧭 codebasetograph (`cbtg`) — a code graph for coding agents
**[royhendriks-dev/codebasetograph](https://github.com/royhendriks-dev/codebasetograph)** · *TypeScript · Node.js*

A local-first CLI that indexes a repository into a queryable graph (files, symbols, imports, dependencies), so AI coding agents can find the relevant code *before* reading source files.

- Indexing needs no LLM and no network; relationships are labelled as extracted, resolved, inferred or unresolved
- Ships a CLI, an MCP server, a prompt hook and an agent skill
- Principle: no token-saving claims without benchmarks on real tasks
- Clean-room implementation with a coverage gate and releases (v1.0.0)

---

## 🏠 Homelab

I run my own platform at home instead of just deploying to someone else's cloud.

```text
git push ─► GitHub Actions ─► tests · coverage · SonarQube Cloud
                │
                └─► multi-arch images (amd64 + arm64) ─► GHCR
                                                          │
          self-hosted runner on a MacBook Air M1 ◄────────┘
                │  kubectl
                ▼
          k3s (Colima) ─► Cloudflare Tunnel + Access ─► royhendriks.com
```

- **Always-on server:** a MacBook Air M1 (8 GB) running k3s, with memory limits on every container and NetworkPolicies between pods.
- **No open ports:** public access runs through a Cloudflare Tunnel; the login sits behind Cloudflare Access.
- **Release flow:** feature PRs go to `develop`; a release PR to `main` is a new semver version that deploys itself and gets a git tag and GitHub Release.
- **Backups:** daily PostgreSQL dumps with a restore test, and a nightly backup CronJob for k3s.
- **Logging:** structured JSON logs, Loki, Grafana and Alloy.
- **Engineering process:** every PR gets a Jira ticket and a Confluence page, and the technical diagrams are kept up to date with the code.

---

## 🤖 Working with AI

I use AI agents as part of my daily workflow: PRs are written, reviewed and documented under clear rules (ticket format, branch strategy, security and accessibility checks), and I'm building tools like `cbtg` to make that work cheaper and more accurate.

---

<div align="center">

*Building software, exploring AI, and learning by creating.*

[royhendriks.com](https://royhendriks.com)

</div>
