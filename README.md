[README-4.md](https://github.com/user-attachments/files/31439061/README-4.md)
<p align="center">
  <a href="#">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&pause=1000&color=2F81F7&center=true&vCenter=true&width=500&lines=Hi%2C+I'm+Srija+Malhar" alt="Typing SVG" />
  </a>
</p>
<p align="center">Full-Stack Engineering, Backend Systems & Applied AI Tooling</p>
<p align="center">React/TypeScript frontends • Correctness-focused backend services • AI-assisted developer tooling</p>

I build full-stack products end to end — React/TypeScript frontends backed by Spring Boot services — with a particular focus on getting the backend right: idempotent writes, transactional integrity, and explicit state machines instead of implicit status flags. That's paired with a Python + LLM-powered code-review tool that automates a task I'd otherwise do by hand.

---

## Featured Projects

| Project | What it does | Tech | Link |
|---|---|---|---|
|  **MiniBee** | Subscription billing microservice — idempotent invoicing proven safe under concurrency via a DB-level constraint, plus a transactional outbox for events | Java · Spring Boot · PostgreSQL · Redis · Kafka | _add link_ |
| **CodeSheriff** | LLM-powered GitHub PR reviewer with inline diff comments, async queue, and a feedback loop | Python · FastAPI · Gemini API | [Repo](https://github.com/SrijaMalhar/codesheriff) |
| **Supply Chain Parts Dashboard** | Tracks parts from supplier to deployment with optimistic UI, audit logs, and inventory valuation | React · Vite · Spring Boot | [Live Demo](https://srijamalhar.github.io/supply-chain-dashboard/) |
| **Predictive Warranty Claim Engine** | Rules-based warranty risk validation with a stateless preview endpoint separate from submission | Java · Spring Boot · React | _add link_ |

<details>
<summary><b>MiniBee — architecture diagram</b></summary>

```mermaid
flowchart TD
    Client["HTTP client / X-API-Key"] --> Controllers["Controllers / DTOs at boundary"]
    Controllers --> Services["Services / rules, @Transactional"]
    Proration["Proration + state machine"] --> Services
    Services --> Repositories["Repositories / Spring Data JPA"]
    Repositories --> DB[("MySQL / PostgreSQL / uk_invoice_sub_period")]
    Repositories --> Outbox["outbox_events / same transaction"]
    Redis["Redis cache / evict-on-write"] --> Services
    Outbox --> Relay["OutboxRelay / polls, publishes"]
    Relay --> Kafka["Kafka"]
    Scheduler["BillingScheduler to BillingRunner / daily, idempotent"] --> DB
```

</details>

---

## Tech Stack

| Category | Technologies |
|---|---|
| **Languages** | ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) |
| **Backend** | ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) |
| **Databases** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![H2](https://img.shields.io/badge/H2-0078D7?style=flat-square) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) |
| **Infra / Messaging** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |
| **AI / Tooling** | ![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) |
| **Testing** | ![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=flat-square&logo=junit5&logoColor=white) ![Testcontainers](https://img.shields.io/badge/Testcontainers-1D63ED?style=flat-square) |

**What's actually used where**

| Technology | Used in |
|---|---|
| Java / Spring Boot | MiniBee, Supply Chain Dashboard, Predictive Warranty Engine |
| React / TypeScript | Supply Chain Dashboard, Predictive Warranty Engine (frontend) |
| Kafka + Redis | MiniBee |
| Docker / Docker Compose | MiniBee, Supply Chain Dashboard |
| Python + Gemini API | CodeSheriff |

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=SrijaMalhar&show_icons=true&theme=default&hide_border=true" alt="GitHub Stats" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=SrijaMalhar&layout=compact&hide_border=true" alt="Top Languages" height="165"/>
</p>



## Let's Connect

<p align="left">
  <a href="https://github.com/SrijaMalhar">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
  <a href="https://www.linkedin.com/in/srija-malhar-252525ss">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
</p>
