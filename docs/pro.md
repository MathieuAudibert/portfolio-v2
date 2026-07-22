---
icon: lucide/briefcase-business
---


## Professional career

### Caisse Primaire d'Assurance Maladie (CPAM) du Val de Marne

Internship during my 3rd year at Efrei as *Concepteur Développeur d'Applications* (Application Designer & Developer) at CPAM94. I worked on two separate projects: AAVA & MouvInvent.

#### AAVA 

As part of my work-study at the CPAM (Primary Health Insurance Fund), I participated in the design, development, and deployment of a business web application. This platform was built to improve tracking and support of nearly 800,000 beneficiaries under campaigns led by the Healthcare Support Mission (MISAS).

This mission — at the core of Health Insurance priorities — aims to contact and support vulnerable populations (elderly individuals, pregnant women, long-term illness patients, complementary health coverage recipients) to improve access to healthcare and legal rights.

The project, AAVA (Accompagnement Automatisé des Visites et Appels), was launched to modernize internal tools. Previous operations relied on large Excel files manually updated by MISAS agents — a process that caused frequent errors, lacked real-time visibility, and wasted significant time.

We designed a centralized, ergonomic, and secure platform offering:

- Beneficiary data entry, editing, and viewing in a few clicks
- Automated import of files from the CNAM (National Health Insurance Fund)
- Real-time campaign progress tracking (contacts made, call reasons, follow-ups)
- Consolidated statistics for operational management
- Structured user management with role-based permissions

The project yielded significant time savings, reduced human error, and improved traceability. It also streamlined communication between stakeholders through a single, reliable, shared database.

**Team Structure**

- Martin: Front-end development and responsive UI design, with focus on accessibility (RGAA compliance)
- Esther: Data modeling, database management, and optimized query writing
- Myself: Full-stack development (Symfony back-end, JavaScript/HTML/CSS front-end) and DevOps

**Technical Stack**

- Symfony (v5) for the back-end
- JavaScript with modular structure for the interactive front-end
- MySQL for data management
- Git versioning via GitLab
- CI/CD pipeline with GitLab CI for controlled deployments

**Methodology & Results**

Launched in December based on specifications co-created with business teams, including requirements-gathering workshops and user testing phases. We worked using an agile approach with iterative deliveries, regular demonstrations, and functional validation in collaboration with MISAS focal points.

AAVA is being progressively deployed across several departmental teams, with planned enhancements including integration with other internal CPAM tools, multi-campaign management, and advanced analytical reporting.

#### MouvInvent

I also participated in the complete front-end and back-end redesign of a local IT hardware management tool used daily by CPAM administrative secretaries and technicians. Built in PHP with a JavaScript interface and MySQL database, the tool tracks IT equipment movements (computers, screens, printers, phones) as well as installation, return, and transfer operations between agents or sites.

Over time, the tool had become slow and unintuitive — aging interfaces made data entry laborious, increased error risk, and often required manual database adjustments.

I was tasked with redesigning the entire tool, both technically and functionally:

- **User experience**: Modern, fluid interface designed around daily needs of field technicians
- **Performance**: Streamlined server calls, reduced load times, improved SQL query management
- **Business logic**: Restructured application logic with proper MVC separation, error handling, validation
- **Security**: Granular user rights management, data protection, operation traceability

Concretely, I:

- Modernized the UI through a full front-end redesign: new interactive components, visual hierarchy, responsive design
- Refactored the PHP code: rationalized controllers, views, database access, with prepared statements for security
- Reworked the data model: normalized tables, added missing relationships, created SQL views for reporting
- Added new features: advanced hardware search, inventory exports, automatic transfer form generation, admin dashboard

The redesign was conducted in close collaboration with end-users through feedback phases, demonstrations, and testing rounds. The new tool led to a significant reduction in time per operation and improved visibility into the IT hardware fleet status.

### Crédit Agricole Assurances (CAAS/CAA)

Currently a Data Engineer apprentice at CAAS alongside my studies at ESILV. I work across multiple projects within the Data Platform team:

#### R4 KPI Digit: KStreams to MongoDB

In CAAS's digital transformation strategy, measuring online journey performance is a top priority: without reliable data on activities across web and mobile policyholder portals, it is impossible to identify friction points, optimize subscription processes, or justify IT investments.

R4 KPI Digit is the Java/Spring Boot microservice that addresses this need: it centralizes KPIs generated by CAAS's digital journeys. Client applications (web/mobile policyholder spaces, advisor tools) emit events on every significant interaction (subscriptions, policy modifications, claim consultations). These events pass through Apache Kafka and are transformed by Kafka Streams according to business rules before being persisted in MongoDB. This database is then consumed by Crédit Agricole Technology & Services (CA-TS) for group reporting.

**My contributions:**

- Implemented the Omnichannel ATM journey — developed transformation rules converting Esesam/CATS events into KPI fields
- Wrote unit tests covering all scenarios specified in mapping files (SonarQube-enforced quality gates)
- Deployed via a three-phase GitOps pipeline (Dev → Pre-prod → Prod) orchestrated by Jenkins, Artifactory, and ArgoCD
- Handled the SonarQube migration from CAAS to CAGIP instance (updated pipelines, resolved dynamic project keys, fixed deprecated API calls)

#### R6 KPI Interne: KSQL to PostgreSQL

While R4 satisfies external reporting requirements for CA-TS, R6 KPI Interne fulfills internal needs: providing CAAS operational teams (actuaries, management control, operational oversight) with a consolidated view of digital activity.

KPIs are persisted into PostgreSQL, exposed via a Denodo data virtualization layer to analytics tools (Power BI for dashboards, SAS for actuarial modeling). Unlike R4, transformations are executed using ksqlDB queries rather than Kafka Streams.

**My contributions:**

- Integrated SonarQube into the Jenkins pipeline — increased unit test coverage from 33% to 76%
- Refactored the "double-brace initialization" anti-pattern (anonymous inner classes causing class-loader overhead)
- Unified life-insurance act topics (arbi-act + veex-act) — eliminated configuration duplication, adapted ksqlDB queries for generic Avro type casting
- Created Kubernetes manifests and integrated ArgoCD deployment into Jenkins pipeline
- Resolved immutable field conflicts in K8s Job resources via pre-deployment deletion steps

#### D6/DataWeb: MongoDB to CSV Shell Export Pipeline

D6 DataWeb is an export pipeline feeding the Dataweb reporting platform. Three Shell scripts query MongoDB collections using aggregation pipelines to produce CSV files covering life insurance financial acts (VLC, VADD, fund reallocations). A concatenation script merges exports and manages historical retention, while a master script orchestrates execution and centralizes logging.

**My contributions:**

- Integrated ShellCheck static analysis and SonarQube scans into the Jenkins pipeline
- Built a custom Docker testing container complying with CAAS security policies (proxy, internal CA certificates, security labeling)
- Consolidated multiple Jenkinsfiles into a single unified pipeline with release management stages
- Implemented kcov-based Shell coverage reporting (Cobertura XML format for SonarQube ingestion)
- Reorganized project structure, standardized log file naming across all five OPC jobs

#### J1 ETFA: Spark performances refactoring

Unit-Linked (UC) life insurance policies link capital values to financial assets. Regulatory mandates require CAAS to publish 10-year historical performance metrics annually for every UC fund.

J1 ETFA is a Spark pipeline that queries Hive tables on a distributed cluster, calculates annual and Year-To-Date performance rates for each fund/contract, and exports CSV datasets.

**My contributions:**

- Resolved accumulated technical debt: refactored duplicated Airflow DAGs, removed unmaintained Oozie workflows, added documentation
- Refactored EtfaPerfDataRecordPrinter using the Bill Pugh Singleton pattern (lazy, thread-safe initialization via static inner class)
- Added structured logging across core classes, updated Jenkins pipelines for Docker publishing and SonarQube analysis
- Developed a new GC_PERF pipeline for Advised Management performance metrics — Spark job with Hive views, window functions, date filtering
- Orchestrated via dedicated Airflow DAG with dynamic node allocation and standard pfd_commons task factories
- Resolved Spark type compatibility issues (Hive inferred types → target output specifications via explicit casting)
