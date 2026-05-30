<div align="center">

# Bishal Acharya

**Backend Engineer · Kathmandu, Nepal · Remote-ready**

[![Available](https://img.shields.io/badge/status-available%20for%20remote%20roles-3B6D11?style=flat&labelColor=EAF3DE)](mailto:acharyabishal172@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-BishalAcharya37-24292e?style=flat&logo=github)](https://github.com/BishalAcharya37)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-bishal--acharya-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/bishal-acharya-47603b269/)
[![Email](https://img.shields.io/badge/email-acharyabishal172@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:acharyabishal172@gmail.com)
[![Live Project](https://img.shields.io/badge/live-acharya--fancy--stores-639922?style=flat&logo=render&logoColor=white)](https://acharya-fancy-stores.onrender.com)

</div>

---

## About

Backend engineer who graduated in 2025 with a **BIT from London Metropolitan University**. I don't just build features — I build systems that hold up when things go wrong.

I think about race conditions before they happen, design rollbacks before writing the happy path, and treat idempotency as a first-class requirement, not an afterthought.

Currently available for **remote backend engineering roles** — I want to be in production, facing real failures, and fixing them.

---

## Tech stack

**Core backend**
`Node.js` `Express.js` `REST API design` `Prisma v7` `PostgreSQL` `MongoDB`

**Data & queuing**
`Redis` `BullMQ` `transactions` `idempotency keys` `distributed locks` `atomic operations`

**Auth & security**
`JWT` `OTP two-factor` `bcrypt` `RBAC` `session management` `trusted devices` `token rotation` `Helmet` `rate limiting`

**Infrastructure & integrations**
`AWS S3` `Cloudinary` `Socket.IO` `webhooks` `Stripe` `Meta Graph API` `Puppeteer` `GitHub Actions` `Docker`

**Validation & observability**
`Zod` `Pino` `structured logging` `audit trails` `Swagger`

**Testing & CI**
`Jest` `Supertest` `integration tests` `CI/CD pipelines`

---

## What I've built

### Acharya Fancy Stores — e-commerce backend &nbsp;[![Live](https://img.shields.io/badge/live-onrender-639922?style=flat)](https://acharya-fancy-stores.onrender.com) [![Repo](https://img.shields.io/badge/repo-github-24292e?style=flat&logo=github)](https://github.com/BishalAcharya37)

`Node.js` `MongoDB` `Redis` `BullMQ` `Stripe` `Cloudinary` `JWT` `Jest` `GitHub Actions`

- Full order lifecycle with **Stripe and Cash on Delivery**. Idempotency keys prevent duplicate orders and payments even under retries or network failures.
- Stripe webhooks with signature validation — `payment_intent.succeeded` and `payment_intent.payment_failed` update order status **atomically**, safe against Stripe retries.
- **Cloudinary image rollback** — new images are uploaded first. If the DB write fails, newly uploaded files are deleted and original URLs restored. No orphaned files, no inconsistency.
- Async transactional email via **BullMQ** — all emails queued and processed by a dedicated worker with exponential backoff retry. The API never waits on email delivery.
- **Refresh token rotation** — every refresh invalidates the previous token. Reuse of an old token triggers immediate full session revocation.
- **Full CI/CD pipeline** — GitHub Actions runs the complete Jest + Supertest suite against a dedicated test database on every push to `main`. Deployment blocked on any test failure.

---

### Production-grade multi-tenant SaaS CRM/ERP

`Node.js` `PostgreSQL` `Prisma` `Redis` `BullMQ` `AWS S3` `Socket.IO` `Meta Graph API` `webhooks` `Puppeteer` `Zod` `Pino`

End-to-end worker lifecycle management built for a real-world client — not a side project.

- **Multi-tenant architecture** — agency-scoped data isolation, per-tenant RBAC, soft deletes with full recovery, and audit logging on every critical mutation.
- **Auth system** — JWT + OTP two-factor, trusted device fingerprinting, session invalidation, office-hours enforcement, and forced password rotation.
- **File workflows** — temp-upload → permanent-move pattern on AWS S3/Cloudinary with atomic rollback on DB failure. Deterministic permanent paths mean updates always overwrite — no accumulation, no orphans.
- **Background job pipelines** — BullMQ queues with retry, exponential backoff, idempotency keys, and dead-letter handling via Redis.
- **Real-time messaging** — Socket.IO with room-based agency isolation. Webhook ingestion from Meta Graph API delivers messages to connected clients instantly.
- **Meta Graph API integration** — Facebook and Instagram page management, post publishing (text, image, multi-image, video), conversation sync, and live inbox with webhook-driven updates.
- **Async PDF reports** — Puppeteer-generated reports queued as background jobs, never blocking the API response.

---

## How I think about backend

| | |
|---|---|
| **Failure first** | What happens when step 2 fails after step 1 succeeds? That's the first question I ask. |
| **Concurrency** | Two users, same resource, same millisecond — race condition? I design around it before it ships. |
| **Idempotency** | If this job runs twice, is the result the same? Background jobs must be safe to retry. |
| **Observability** | Structured logs, audit trails, enough context to debug at 2am without reading every line. |
| **Simplicity** | The boring solution that works beats the clever one that breaks under edge cases. |
| **Shipped & tested** | CI/CD and tests before calling anything done. I don't push untested code. |

---

<div align="center">

**Open to remote backend engineering roles — available immediately.**

[acharyabishal172@gmail.com](mailto:acharyabishal172@gmail.com) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/bishal-acharya-47603b269/) &nbsp;·&nbsp; [GitHub](https://github.com/BishalAcharya37)

</div>
