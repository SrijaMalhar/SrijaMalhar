<h1 align="center">Hi, I'm Srija Malhar 👋</h1>
<p align="center">Building Correct, Concurrent Backend Systems</p>
<p align="center">Backend engineering focused on transactional correctness • Full-stack delivery • AI-assisted developer tooling</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=SrijaMalhar&color=blue&style=flat-square&label=PROFILE+VIEWS" alt="Profile Views"/>
</p>

I build backend systems where correctness under concurrency isn't an afterthought — idempotent writes enforced at the database, transactional outboxes instead of dual writes, explicit state machines instead of implicit status flags. That work is paired with React/TypeScript frontends to ship full products, and with a Python + LLM-powered code-review tool that automates a task I'd otherwise do by hand.

---

## Featured Projects

### [MiniBee](#) — Subscription Billing & Invoicing Microservice
A Chargebee/Stripe-Billing-style service where invoice generation is idempotent per subscription and billing period, even under concurrent or re-fired requests.

**Problem:** Billing systems fail expensively when a race condition or retried job produces the same invoice twice. Application-level checks alone can't close that race.
**Built with:** Java 17, Spring Boot 3.3, Spring Data JPA, MySQL/PostgreSQL, Redis, Kafka, JUnit 5 + Testcontainers, Docker
**Engineering:** Idempotency is enforced with a database-level `UNIQUE(subscription_id, billing_period)` constraint rather than an application check — proven under a 20-thread concurrent integration test. Events are published via a transactional outbox to avoid the dual-write problem, and plan changes are prorated through an explicit subscription state machine.
**Repository:** _add link_

### [CodeSheriff](https://github.com/SrijaMalhar/codesheriff) — Automated GitHub PR Reviewer
An LLM-powered PR reviewer that posts inline comments on the exact diff line, with a feedback loop that improves future reviews.

**Problem:** Manual PR review doesn't scale, and most automated linters miss cross-file context.
**Built with:** Python, FastAPI/Uvicorn, Google Gemini API, GitHub Webhooks, SQLite, GitHub Actions
**Engineering:** Runs an async background queue so the webhook responds instantly while review happens out-of-band, and a shadow mode lets the reviewer analyze PRs silently before it's trusted to post. A thumbs-up/down feedback loop is stored and exportable for tuning review quality over time.
**Repository:** [github.com/SrijaMalhar/codesheriff](https://github.com/SrijaMalhar/codesheriff)

### [Supply Chain Parts Traceability Dashboard](#) — Parts Tracking & Inventory Dashboard
Tracks spare parts from supplier → warehouse → assembly → deployed, with supplier health, audit logs, and inventory valuation.

**Problem:** Manufacturing supply chains need real-time visibility into where a part is and what it's worth at each stage.
**Built with:** React 18 + Vite, Spring Boot 3 (Java 17), H2, Docker Compose, Swagger/OpenAPI
**Engineering:** Optimistic UI updates with rollback on error, plus live duplicate-part detection while adding new inventory — small details that make the dashboard feel responsive rather than form-driven.
**Repository:** [srijamalhar.github.io/supply-chain-dashboard](https://srijamalhar.github.io/supply-chain-dashboard/)

### [Predictive Warranty Claim Engine](#) — Rules-Based Warranty Risk Validation
Applies manufacturing-style warranty rules to flag high-risk claims for heavy machinery, with an explainable risk indicator rather than a black-box score.

**Problem:** Warranty fraud and abuse detection needs to be explainable to a claims team, not just accurate.
**Built with:** Java 17, Spring Boot 3.2, Spring Data JPA, React + Tailwind, H2 (Postgres-compatible mode)
**Engineering:** Separates a stateless "preview" validation endpoint from the persisting "submit" endpoint, so a claim's eligibility and risk score can be checked live before anything is written — with rejections returning a structured `422` rather than a generic error.
**Repository:** _add link_

---

## Tech Stack

**Languages**
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**Backend**
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Databases**
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![H2](https://img.shields.io/badge/H2-0078D7?style=flat-square)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**Infra / Messaging**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**AI / Tooling**
![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

**Testing**
![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-1D63ED?style=flat-square)

| Technology | Used in |
|---|---|
| Java / Spring Boot | MiniBee, Supply Chain Dashboard, Predictive Warranty Engine |
| React / TypeScript | Supply Chain Dashboard, Predictive Warranty Engine (frontend) |
| Kafka + Redis | MiniBee |
| Docker / Docker Compose | MiniBee, Supply Chain Dashboard |
| Python + Gemini API | CodeSheriff |

---


## Connect

- GitHub: [@SrijaMalhar](https://github.com/SrijaMalhar)
