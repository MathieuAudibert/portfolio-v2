---
icon: lucide/square-arrow-right-exit
---

# Local Machine Learning Flow

Local-ml-flow is a home project combining technologies and concepts I want to deepen. It's a local MLOps ecosystem designed to automate the machine learning lifecycle through local cloud computing (LocalStack) and a GitHub Actions workflow.

The README is detailed and explains through Mermaid schemas, wiki links, and LaTeX the project's runtime. There is also a "Future" chapter outlining planned improvements and modifications.

Links:
• GitHub: https://github.com/MathieuAudibert/local-ml-flow
• GitHub package: https://github.com/MathieuAudibert/local-ml-flow/pkgs/container/local-ml-flow

# BankWerk

Crypto-oriented online bank. BankWerk is a Node/Next.js project made at school.
I managed the back-end/Google Cloud/Firebase infrastructure and the crypto-fetching API (CoinMarketCap).

# Eco-Pulse 

ELT pipeline to ingest global carbon emissions.

This project builds a production-grade ELT (Extract, Load, Transform) pipeline that ingests global carbon emission datasets from Kaggle. It utilizes Docker and Airflow for orchestration, with Python handling the data logic. A key feature is the integration of Aiven for Valkey as a centralized, high-speed configuration store to manage environment variables and API keys dynamically — sensitive credentials never reside in the local codebase.

**Technical stack:**

- Python
- Docker
- Airflow
- Aiven for Valkey
- Cloud
    - Backblaze B2 (dataset object storage)
    - GCP (PostgreSQL analytics database)
- Kaggle API

# Leboncours 

A Single Page Application (SPA) where users sign up as Teachers or Students. Teachers offer courses with availability slots, and students browse and book sessions. The platform includes an admin role, a messaging system, and a dashboard with charts.

**Backend:**

- Language: Rust (Edition 2024)
- Framework: Axum 0.7
- Async Runtime: Tokio
- ORM: SeaORM 1.1 (PostgreSQL via sqlx)
- API Docs: Utoipa + Swagger UI
- Auth: Argon2 (password hashing) + JWT
- CORS: tower-http

**Database:**

- System: PostgreSQL
- Schema management: Raw SQL (db/create_table.sql)

**Frontend:**

- Framework: React 19
- Language: JavaScript (JSX)
- Routing: react-router-dom 7
- Data Grid: AG Grid React 35
- Charts: Recharts
- Icons: Lucide React, React Icons
- Auth State: React Context with sessionStorage
