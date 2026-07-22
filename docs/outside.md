---
icon: lucide/square-arrow-right-exit
---

# Local Machine Learning flow

Local-ml-flow is a home project, combining the technologies and concept I want to improve in. It's a local MLOps ecosystem designed to automate machine learning lifecycle through local cloud computing (LocalStack) and a Github actions workflow. 

The README is detailled and explains through mermaid schemas, wiki links and LaTeX the project's runtime. There is also a "Future" chapter where I explain what I would like to implement/modify on the project. 

Links : 
• Github : https://github.com/MathieuAudibert/local-ml-flow
• Github package : https://github.com/MathieuAudibert/local-ml-flow/pkgs/container/local-ml-flow

# BankWerk

Online crypto-oriented bank, Bankwerk is a Node/NextJS project made at school.
I managed the back-end/Google Cloud/Firebase infrastructure and the crypto-fetching API (cryptos https://coinmarketcap.com/api/)

# Eco-pulse 

ELT pipeline to ingest global carbon emissions
Objectives

This project builds a production-grade ELT (Extract, Load, Transform) pipeline that ingests global carbon emission datasets from Kaggle. It utilizes Docker and Airflow for orchestration, with Python handling the data logic. A unique security feature is the integration of Aiven for Valkey as a centralized, high-speed configuration store to manage environment variables and API keys dynamically, ensuring that sensitive credentials never reside in the local codebase.
Technical stack

    Python
    Docker
    Airflow
    Aiven for Valkey
    Cloud
        Backblaze B2 (for dataset object storage)
        GCP (for Postgres analytics db)
    Kaggle API

# Leboncours 

Leboncours

A Single Page Application (SPA) where users can sign up as Teachers or Students. Teachers offer courses with availability slots, and students can browse and book sessions. The platform also includes an admin role, a messaging system, and a dashboard with charts.
Tech Stack
Backend

    Language: Rust (Edition 2024)
    Framework: Axum 0.7
    Async Runtime: Tokio
    ORM: SeaORM 1.1 (PostgreSQL via sqlx)
    API Docs: Utoipa + Swagger UI
    Auth: Argon2 (password hashing) + JWT (jsonwebtoken)
    Validation: validator
    CORS: tower-http

Database

    System: PostgreSQL
    Schema management: Raw SQL (db/create_table.sql)

Frontend

    Framework: React 19 (Create React App)
    Language: JavaScript (JSX)
    Routing: react-router-dom 7
    Data Grid: AG Grid React 35
    Charts: Recharts
    Icons: Lucide React, React Icons
    HTTP Client: Native fetch (custom wrapper in src/api.js)
    Auth State: React Context (AuthContext) with sessionStorage
