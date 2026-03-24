# Kulshresth Jangid

**Backend Engineer · Systems Architect · Jaipur, India**  
Software Engineer at [Equinix](https://equinix.com) · Self-taught · Building production systems since 2020

---

## What I Build

I design and ship backend-heavy systems: async pipelines, distributed architectures, and real SaaS products from schema to Kubernetes. Not tutorials. Not demos.

Current focus: multi-tenant SaaS, event-driven systems, and AI integration at the infrastructure level.

---

## Lumen — Marketing Operating System

The most complex system I've built and shipped. Founded it.

**Architecture (production):**

```
tic-tac-toe (:443, reverse proxy)
├── /app         → echo-post    (Next.js frontend)
└── /api/v1/     → smart-server (Spring Boot, :8080)
```

**What it does:**  
Four-stage async pipeline — Source ingestion → Insight extraction → Post generation → Distribution. RabbitMQ between each stage. Every stage fails independently, retries with backoff, and writes to a dead-letter queue.

**Scale decisions I made:**
- Redis time-wheel for 1M+ concurrent scheduled tasks per instance
- BYO-AI layer: provider-agnostic LLM client, org-level config stored encrypted — no model lock-in
- Multi-tenant PostgreSQL with row-level security per org
- Three automation modes: Manual / Review / Autopilot — operates correctly at each

**Stack:** Java · Spring Boot · Next.js · TypeScript · RabbitMQ · Redis · Elasticsearch · PostgreSQL · Kubernetes · Docker

→ [Live system](https://tic-tac-toe.kulshresth.dev/app) · [Source (frontend)](https://github.com/KulshresthJangid/echo-post-frontend) · [Source (backend)](https://github.com/KulshresthJangid/SMAT)

---

## Monolith → Microservices Migration (Equinix / Rampwin)

Led domain decomposition and phased service extraction under real production constraints.

**What I actually did:**
- Event storming to define bounded contexts before any code changed
- Strangler fig extraction with feature-flag traffic routing at the Nginx layer
- Kafka as the inter-service event fabric — async, replay-capable, no direct coupling
- Distributed sagas for cross-service transactions (checkout, order lifecycle)
- Pact contract testing in CI — breaking changes caught before staging

**Outcome:** MTTR reduced 28%. Cross-domain failures became structurally impossible. Teams deploy independently.

**Stack:** Java · Spring Boot · Kafka · MongoDB · Kubernetes · Istio · Jaeger

---

## Engineering Principles

**On architecture:**  
I start from failure modes, not happy paths. Every system I design has an explicit answer to: what happens when this component is unavailable?

**On async systems:**  
I default to event-driven when latency tolerance allows. Synchronous chains are coupling in disguise.

**On scale:**  
I don't pre-optimize, but I design for the next order of magnitude. Schema decisions and data ownership boundaries are hard to undo later.

**On tradeoffs I've made:**  
- Chose at-least-once delivery + idempotent consumers over exactly-once. Operationally simpler under failure.
- Chose row-level security over separate schemas per tenant. Simpler migrations, acceptable performance tradeoff at current scale.
- Chose BYO-AI over hosted model. Reduces cost and removes lock-in for customers — added complexity in the provider abstraction layer was worth it.

---

## Stack

**Primary:** Java · Spring Boot · TypeScript · Node.js · Next.js  
**Data:** PostgreSQL · MongoDB · Redis · Elasticsearch · DynamoDB  
**Infra:** Docker · Kubernetes · Kafka · RabbitMQ · Jenkins  
**Cloud:** AWS · Equinix Metal

---

## Contact

I'm open to backend architecture roles, founding engineer positions, and early-stage SaaS.

[LinkedIn](https://linkedin.com/in/kulshresth-jangid) · kulshresthjangid@gmail.com
