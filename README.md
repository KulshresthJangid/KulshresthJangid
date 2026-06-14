# Kulshresth Jangid — Backend Engineer · Systems Architect

Software Engineer at **Equinix**. I build distributed backend systems — async pipelines, event-driven architectures, and production-grade SaaS. Based in Jaipur, India.

📦 **Lumen** (my flagship project) → [buildwithkulshresth.com/app](https://buildwithkulshresth.com/app) — multi-tenant marketing OS with a 4-stage async pipeline, Redis time-wheel (1M+ concurrent tasks), provider-agnostic LLM layer, and row-level security PostgreSQL on Kubernetes.

---

## What I've Shipped

### Lumen — Marketing Operating System

*Self-founded · Java · Spring Boot · Next.js · RabbitMQ · Redis · PostgreSQL · Kubernetes*

- **4-stage async pipeline** via RabbitMQ (generation → review → scheduling → delivery)
- **Redis time-wheel** managing 1M+ concurrent scheduled tasks
- **Multi-tenant PostgreSQL** with row-level security — no schema-per-tenant complexity
- **Provider-agnostic LLM client** — orgs bring their own API key, encrypted at rest
- Three automation modes: Manual, Review, Autopilot

### Monolith → Microservices Migration @ Equinix / Rampwin

*Java · Kafka · Docker · Kubernetes · Pact (contract testing)*

- Domain decomposition via event storming + strangler fig pattern
- Kafka event fabric with distributed sagas for cross-service consistency
- Pact contract testing to prevent integration regressions
- **Result: 28% reduction in MTTR**, independent team deployments

---

## Engineering Principles

- **Failure-mode-first design** — model failure before success paths
- **Event-driven by default** — decoupled async systems that scale independently
- **Intentional tradeoffs** — at-least-once + idempotent consumers; row-level security over schema-per-tenant; bring-your-own-AI over vendor lock-in

---

## Stack

| Layer | Tech |
|---|---|
| Languages | Java, TypeScript, JavaScript |
| Frameworks | Spring Boot, Next.js |
| Data | PostgreSQL, MongoDB, Redis, Elasticsearch, DynamoDB |
| Messaging | Kafka, RabbitMQ |
| Infra | Docker, Kubernetes, Jenkins, AWS, Equinix Metal |

---

## Let's Talk

Open to **backend architecture roles** (Staff/Senior) — distributed systems, platform engineering, SaaS infrastructure.

📧 [jangidkulshresth@gmail.com](mailto:jangidkulshresth@gmail.com) · [LinkedIn](https://linkedin.com/in/kulshresth-jangid) · [buildwithkulshresth.com](https://buildwithkulshresth.com)
