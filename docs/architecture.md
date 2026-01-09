┌─────────────────────────┐
│       Frontend          │
│   (Next.js Dashboard)   │
---------------------------
            │ HTTPS
┌───────────┴─────────────┐
│     FastAPI Backend     │
│  (API Gateway Layer)    │
---------------------------
            │
-----------------------------------
│        Core Services            │
│                                 │
│  Auth & RBAC Service            │
│  User & Profile Service         │
│  Document Management Service    │
│  AI Analysis Service            │
│  Credit Risk Engine             │
│  Payment & Subscription Service │
│  Audit & Logging Service        │
-----------------------------------
            │
----------------------------------
│        Data Layer              │
│                                │
│  PostgreSQL (Core Data)        │
│  Vector DB (Chroma)            │
│  Object Storage (Docs)         │
----------------------------------
