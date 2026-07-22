---
icon: lucide/briefcase-business
---


## Professional career

### Caisse Primaire d'Assurance Maladie (CPAM) du Val de Marne

I did an internship during my 3rd year @ Efrei. I was "Concepteur Développeur d'Applications" (Application Designer & Developer) @ CPAM94. 

During my time at CPAM I worked on 2 separate projects : AAVA & MouvInvent

#### AAVA 

As part of my work-study program at the CPAM (Primary Health Insurance Fund), I had the opportunity to actively participate in the design, development, and deployment of a business web application. This platform was designed to improve the tracking and support of nearly 800,000 beneficiaries under campaigns led by the Healthcare Support Mission (Mission Accompagnement Santé - MISAS).

This mission—at the core of Health Insurance priorities—aims to contact and support the most vulnerable populations (elderly individuals, pregnant women, patients with long-term illnesses [ALD], beneficiaries of complementary health coverage [CSS], etc.) to enhance access to healthcare and legal rights.

The project, named AAVA (Accompagnement Automatisé des Visites et Appels / Automated Support for Visits and Calls), was launched with a clear objective: modernize internal tools. Previous operations relied on a time-consuming and unreliable data management process using large Excel files manually updated by MISAS agents. Although functional, this approach caused frequent errors, a lack of real-time visibility into ongoing operations, and significant time loss.

Face to face with these issues, we designed a centralized, ergonomic, and secure platform, offering a user-friendly interface tailored to the needs of business teams. Thanks to AAVA, agents can now:

- Enter, edit, and view beneficiary data in just a few clicks.

- Automate the import of files regularly provided by the CNAM (National Health Insurance Fund).

- Track campaign progress in real time (contacts made, call reasons, required follow-ups).

- Generate consolidated statistics for operational management.

- Manage users in a structured manner based on defined roles and permissions.

This project yielded significant time savings, a reduction in human error risks, and better traceability of actions taken. It also streamlined communication between stakeholders through a single, reliable, and shared database.
Team Structure

Three work-study students were assigned to this project:

- Martin: In charge of front-end development and responsive UI design, paying special attention to accessibility (RGAA compliance) and ergonomics.

- Esther: Responsible for data modeling, database management, and writing optimized queries to guarantee performance.

- Myself: Contributing cross-functionally to full-stack development (Symfony back-end and JavaScript/HTML/CSS front-end), while also handling DevOps tasks.

Technical Stack

From a technical perspective, the project relies on:

- Symfony (v5) for the back-end, ensuring code robustness and maintainability.

- JavaScript with a modular structure for the interactive front-end.

- MySQL for data management.

- Collaborative Git versioning via GitLab.

- A CI/CD pipeline set up with GitLab CI, enabling smooth and controlled deployments of updates to test and production environments.

Project Methodology & Results :

The project launched in December, based on specifications co-created with the business teams, including several requirements-gathering workshops and real-world user testing phases. Since then, we have worked using an agile approach, featuring iterative deliveries, regular demonstrations, and functional validation phases carried out in close collaboration with MISAS focal points.

This experience allowed me to develop numerous technical, organizational, and interpersonal skills, including understanding business challenges, project management, communicating with end-users, and adapting to health data security and confidentiality constraints.

Today, AAVA is being progressively deployed across several departmental teams. Enhancements are already planned, including integration with other internal CPAM tools, multi-campaign management, and advanced analytical reporting modules.

#### MouvInvent

Here is the clean, formatted English translation ready to copy and paste:

I also participated in the complete front-end and back-end redesign of a local IT hardware management tool used daily by CPAM administrative secretaries and technicians. Historically developed in PHP with a JavaScript interface and a MySQL database, the initial purpose of this internal tool was to track IT equipment movements (computers, screens, printers, phones, etc.), as well as installation, return, or transfer operations between agents or sites.

Over time, the tool showed its limits in terms of ergonomics, clarity, and performance. Aging and unintuitive interfaces made data entry laborious, increased the risk of errors, and often required manual database adjustments. Many users expressed frustration regarding the application's slowness and lack of functional clarity.

Faced with this issue, I was tasked with redesigning the entire tool, both technically and functionally. This redesign pursued several objectives:

- Improve user experience: By proposing a more modern, fluid interface designed around the concrete daily needs of field technicians.

- Optimize performance: By streamlining server calls, reducing load times, and improving SQL query management.

- Reinforce business logic consistency: By restructuring application logic and ensuring better separation of concerns in the code (MVC, error handling, validation, etc.).

- Secure the application: By adding granular user rights management, better data protection, and operation traceability.

Concretely, I:

- Modernized the user interface through a full front-end redesign: new interactive components, visual information hierarchy, more intuitive navigation, responsive design, etc.

- Refactored the PHP code: Rationalized controllers, views, and database access, using prepared statements more effectively to strengthen security.

- Reworked the data model: Normalized certain tables, added missing relationships, and created new SQL views to facilitate reporting and exports.

- Added new features: Advanced hardware search, inventory exports, automatic generation of transfer forms, and a summary dashboard for administrators.

This redesign was conducted in close collaboration with end-users through several feedback phases, intermediate demonstrations, and testing rounds. Thanks to their feedback, we were able to refine priorities, fix potential bottlenecks, and deploy a solution genuinely tailored to field needs.

The new tool was rolled out progressively to production alongside user support for onboarding. It quickly led to a significant reduction in time spent per operation, as well as improved visibility into the status of the IT hardware fleet. This project was an excellent opportunity for me to consolidate my full-stack development skills, database optimization, project management, and change management capabilities.

### Crédit Agricole Assurances (CAAS/CAA)

Currently, I am a Data-Engineer intern @ CAAS and Esilv. 

I had the occasion to work on a multitude of projects : 

#### R4 KPI Digit: KStreams to MongoDB

In CAAS's digital transformation strategy, measuring online journey performance is a top priority: without reliable data on activities across web and mobile policyholder portals, it is impossible to identify friction points, optimize subscription processes, or justify IT investments to business stakeholders.

R4 KPI Digit is the Java/Spring Boot microservice that addresses this need: it centralizes Key Performance Indicators (KPIs) generated by CAAS’s digital journeys. Client applications (web/mobile policyholder spaces, advisor tools) emit events upon every significant interaction (subscriptions, policy modifications, claim consultations, etc.). These events pass through Apache Kafka and are transformed by Kafka Streams according to business rules before being persisted in a MongoDB database. This database is then consumed by Crédit Agricole Technology & Services (CA-TS), which aggregates and integrates the data into their IT ecosystem.

The objective is twofold:

- Provide CA-TS with reliable and comprehensive KPIs for group reporting.

- Ensure data historization and reliability.

Estimation / Costing: Every new feature is first estimated with Business Analysts (BAs) prior to development. This exercise involves reviewing the BA-provided mapping document—which outlines transformation rules line-by-line—and estimating the man-days required for implementation and testing.In the absence of formal estimation models, estimation relies heavily on cumulative sprint experience. Early in the work-study program, my estimates were calibrated and adjusted by senior developers based on their domain knowledge. Gradually, I became capable of estimating independently based on previous experience.Development: My contributions focused on implementing the Omnichannel ATM journey. I developed and resolved transformation rules converting Esesam/CATS events into KPI fields.Example 1 (Technical Communication Code): Depending on the event type (initial vs. final signature) and the subscription channel (branch, mobile, web), the rule outputs a three-digit code defined in the mapping document.Example 2 (TOP_EVT_FINAL boolean field): Indicates whether a received event is the final event of a transaction. The business rule distinguishes between a final signature (SUBSCRIPTION_SIGNATURE_END) and an initial signature on a new Esesam (SUBSCRIPTION_SIGNATURE_INIT + isNewSesame = true), both representing the completion of an action.Testing: Code quality is an enforced constraint within the Data Platform (PFD), monitored via SonarQube. For every rule implemented, I wrote unit tests covering all scenarios specified in the mapping file (e.g., verifying CD_TECHNCOMMUNICATION_CODE across event-type and channel combinations).Deployment: Deployments follow a three-phase GitOps pipeline (Development $\rightarrow$ Pre-production $\rightarrow$ Production) orchestrated by Jenkins, Artifactory, and ArgoCD. I independently deployed to the development environment and assisted AppOps teams with promotions to pre-production and production environments.Challenges Encountered and SolutionsMapping Consistency with Code: Certain mapping rules were incomplete, particularly regarding conditions for detecting a "new Esesam." I collaborated with BAs to eliminate ambiguities prior to development and updated the mapping documentation alongside code changes.SonarQube Migration (CAAS $\rightarrow$ CAGIP): The project was impacted by the migration from CAAS's standalone SonarQube instance to the shared CAGIP (Crédit Agricole Group Infrastructure Platform) instance. Driven by the expiration of the CAAS license on March 20 and a desire to consolidate parallel instances, the group migrated to CAGIP. I updated Jenkins pipelines, resolved dynamic project keys from pom.xml, and fixed deprecated SonarQube API calls.Results AchievedAll management rules for the Omnichannel ATM journey were successfully deployed to production.

#### R6 KPI Interne: KSQL to PostgreSQL

While R4 satisfies external reporting requirements for CA-TS, R6 KPI Interne fulfills a symmetric internal need: providing CAAS operational teams with a consolidated view of digital activity for internal analysis.Operational teams (actuaries, management control, operational oversight) utilize specialized analytics tools (Power BI for monitoring dashboards, SAS for actuarial modeling). R6 performs the required data transformation: KPIs are persisted into a relational PostgreSQL database, exposed via a Denodo data virtualization layer to unify data access without duplicating data stores.The practical impact is clear: an actuary lacking reliable data on policy reallocations or lump-sum payments cannot accurately calibrate risk models. Missing or inaccurate KPIs can propagate all the way to regulatory reporting submitted to the ACPR (Prudential Costs and Resolution Authority).Unlike R4, transformations are executed using ksqlDB queries (Apache Kafka's continuous SQL engine) rather than Kafka Streams.Tasks PerformedSonarQube Integration into Jenkins Pipeline: The project previously lacked automated static code analysis. I introduced a Sonar analysis stage into the Jenkinsfile. Given the multi-module Maven project structure, I configured the stage to target only core business modules to avoid scanning non-testable artifacts (e.g., schemas).Through iterative testing additions, unit test coverage for the migration module increased from 33% to 76%.Refactored instances of the "double-brace initialization" anti-pattern in Java. This idiom creates anonymous inner classes inheriting from the target type, leading to readability issues and JVM class-loader overhead (memory bloat).Unification of Life-Insurance Act Topics: Initial configurations declared arbi-act (reallocations) and veex-act (exceptional payments) as distinct inputs in properties, each with its own Avro schema. Because both journeys share identical downstream processing logic, this duplication increased maintenance overhead.Re-architected configuration to unify topics.Adapted ksqlDB queries to cast generic Avro types into target types explicitly within ksqlDB streams.Kubernetes/ArgoCD Deployment: Created Kubernetes manifests for migration and history modules and integrated ArgoCD deployment steps into the Jenkins pipeline. The procedure explicitly deletes existing Kubernetes Job objects via argocd CLI prior to triggering deployments to prevent immutable field update conflicts.Challenges Encountered and SolutionsTechnical Debt and Quality Gates: Initial SonarQube runs flagged multiple code smells. I introduced an incremental strategy: Quality Gates were initially restricted to new code (New Code Period feature), enabling team members to remediate legacy technical debt sprint-by-sprint without blocking ongoing feature deliveries.SonarQube Migration (CAAS $\rightarrow$ CAGIP): Handled Jenkins agent Docker images, updated URLs/tokens, and resolved custom SSL certificate validations required by CAGIP infrastructure.Immutable Field Conflicts in ArgoCD: ArgoCD rejected updates to Kubernetes Job resources due to immutable field constraints (e.g., pod selectors). Implemented a pre-deployment step deleting existing jobs via argocd app delete-resource in the pipeline.Results AchievedSonarQube static analysis executes automatically on every merge request via the CAGIP instance, maintaining test coverage at 76%. The life-insurance topic refactoring eliminated duplicate configurations, and Kubernetes/ArgoCD deployments are fully automated in Jenkins.

#### D6/DataWeb: MongoDB to CSV Shell Export Pipeline

Context and ObjectivesExposing data as CSV files is a common requirement across CAAS. D6 DataWeb is an export pipeline developed by the Data-Value squad feeding the Dataweb reporting platform used by commercial and steering teams.Exported datasets cover three financial act types on life insurance products: flexible ad-hoc payments (VLC), additional top-up payments (VADD), and fund reallocations.Three Shell scripts query corresponding MongoDB collections using aggregation pipelines to produce CSV files. A concatenation script (d6_concatenate.sh) merges these exports and manages historical retention, while a master script (export_dtwb.sh) orchestrates execution and centralizes log management and error codes. Final CSVs are transferred to Dataweb via five scheduled OPC jobs (CRON equivalent).Initially, the project lacked static analysis and test coverage. My work focused on four key areas:Code and Jenkins pipeline refactoring.Creating a dedicated testing Docker container.Enhancing logging infrastructure.Integrating static analysis.Tasks PerformedCI/CD Integration and Static Analysis: Integrated ShellCheck static analysis into the Jenkins pipeline and configured SonarQube scans pointing to the CAGIP endpoint.Docker Infrastructure: Built a custom Docker image complying with CAAS security policies, incorporating required proxy settings, internal CA certificates (cacerts), and security labeling.Pipeline Consolidation: Merged multiple scenario-specific Jenkinsfiles into a single unified Jenkinsfile with release management stages.Refactoring & Logging: Reorganized project directory structures by placing executable scripts into a dedicated bin/ folder, simplified scripts into concise one-liners where appropriate, and standardized log file naming conventions across all five OPC jobs.Challenges Encountered and SolutionsShell Code Coverage via kcov: Measuring coverage on Shell scripts cannot be accomplished with standard tools (e.g., JaCoCo). Selected kcov as the execution engine; integrating it within a restricted Docker environment (proxies, internal certs) required multiple base-image iterations to comply with Data Platform guidelines.SonarQube Configuration for Shell: Configured manual reporting conversions using Cobertura XML format to allow SonarQube to ingest ShellCheck static analysis and coverage metrics properly.Results AchievedAll developed enhancements were successfully deployed to the development environment, improving log verbosity. Production rollout remains pending, subject to potential project-wide architectural refactoring.

#### J1 ETFA: Spark performances refactoring

Unit-Linked (Unités de Compte - UC) life insurance policies link capital values directly to financial underlying assets (stocks, bonds, funds). Regulatory mandates require CAAS to publish 10-year historical performance metrics annually for every UC fund, helping policyholders and advisors evaluate investment performance.

J1 ETFA (Export des Tableaux de Performances Annuelles) is a Spark pipeline managed by the PerfOpe squad. It queries Hive tables on a distributed cluster, calculates annual and Year-To-Date (YTD) performance rates for each fund/contract, and exports CSV datasets consumed by the platform.
Tasks Performed

    Refactoring and Onboarding: Resolved accumulated technical debt: Airflow DAGs duplicated code blocks across sites without abstraction, legacy Oozie workflows were unmaintained, and documentation was absent.

        Refactored EtfaPerfDataRecordPrinter in Java using the Bill Pugh Singleton pattern. This pattern leverages a static inner class (SingletonHelper) loaded by the JVM only upon the first getInstance() call, providing lazy, thread-safe initialization without explicit synchronized overhead.

        Added structured logging across PlugEmbEtfaPerf and Utils. Updated Jenkins pipelines to support Docker publishing and SonarQube analysis.

    New GC_PERF Pipeline: Developed a new extraction pipeline for Gestion Conseillée (Advised Management) performance metrics based on BA functional mappings.

        The Spark job (PlugEmbGcPerf.java) constructs views by loading Hive datasets (D3_ZE_OMTR_POL_TTE_GAM, D3_ZE_OMTR_PFM), filtering active Advised Management policies, and computing TX_PRF_Q (YTD performance rate) using window functions partitioned by contract. Applied date filtering (geq(lit(2025))) to restrict the historical window.

        Extracted ten annual columns (an0–an9) alongside fixed fields from ${usg:etfa.j1.j1_zo_gc_perf} representing a 10-year historical timeline.

        Orchestrated pipeline execution via a dedicated Airflow DAG (usage_etfa_gc_perf.py), utilizing dynamic node allocation (get_nb) and standard pfd_commons task factories (generate_gc, export_gc, copy_file).

Challenges Encountered and Solutions

    Spark Data Type Compatibility: Inferred types from Hive/MapR tables differed from target output specifications. Explicitly cast date fields using .cast("string").substr(1,4).cast("int") for annual filtering. Converted TX_PRF_Q using .multiply(100.0) followed by .round(..., 2) to meet the required DECIMAL(8,10) database precision.

Results Achieved

The project now includes comprehensive documentation, a working Jenkins CI/CD pipeline with SonarQube quality gates, and a maintainable Airflow DAG. Production deployment is scheduled for July.