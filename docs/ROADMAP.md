\# Project Roadmap

\#\# Project Vision  
A modular, scalable Banking CRM built initially as a Google Sheets MVP and evolving into a full-stack, compliance-ready solution.    
Long-term, the project integrates analytics and AI/ML for intelligent insights and proactive compliance.

\---

\#\# Phase v1.0 (Current – MVP)

\*\*Tech:\*\* Google Sheets \+ Apps Script    
\*\*Focus:\*\* Proof-of-concept, quick iteration, business logic validation  

\*\*Architecture Layers\*\*  
\- \*\*Presentation Layer:\*\* Conditional formatting, lookup-driven dropdowns, AUM Dashboard    
\- \*\*Application Layer:\*\* Apps Script functions for data generation, validation, automation, and calculations    
\- \*\*Data Access Layer:\*\* Sheet formulas (\`VLOOKUP\`, \`FILTER\`) and Apps Script queries    
\- \*\*Data Layer:\*\* Sheets (\`Customer\_Master\`, \`Staff\_Master\`, \`Sales\_Funnel\`, \`Opportunity\`, \`Appointment\`, \`Lookups\`)    
\- \*\*Integration Layer:\*\* None (self-contained within Sheets)  

\*\*Core Architecture\*\*  
\- \*\*Staff\_Master\*\* – staff registry with roles, branches, and status    
\- \*\*Customer\_Master\*\* – customer profiles, demographics, AUM, segmentation, and RM assignments    
\- \*\*Lookups\*\* – centralized reference tables (roles, segments, tiers, regions, activity/product types, statuses)    
\- \*\*Sales\_Funnel\*\* – lead engagement tracking with status, RM ownership, and last-contacted dates    
\- \*\*Opportunity\*\* – opportunity pipeline with sales volume, probability, expected close date, and linkage to funnel    
\- \*\*Appointment\*\* – customer appointments linked to opportunities or customers, with activity type, status, outcome, and follow-ups    
\- \*\*AUM\_Dashboard\*\* – portfolio insight dashboard using pivot tables and charts

\*\*Validation Rules (Baseline)\*\*  
\- Standardized dropdowns from \`Lookups\` (roles, region, segment, tier, etc.)    
\- Email format checks    
\- Phone number format checks    
\- AUM consistency with product balances (CASA, FD, UT, SP, Bond, Banca, CC)    
\- Duplicate prevention on Staff\_ID, CIF, Funnel\_ID, Opty\_ID, and Appt\_ID  

\*\*UX Streamlining (Baseline)\*\*  
\- Lookup-driven dropdowns for consistent entry    
\- Conditional formatting for statuses, tiers, aging, and overdue items    
\- Color scales for engagement, AUM band, risk profile, probability, and activities    
\- Stale-contact warnings and overdue highlights for opportunities/appointments  

\*\*Documentation\*\*  
\- ERD (Entity Relationship Diagram)    
\- BRD (Business Requirements Document)    
\- ROADMAP.md    
\- CHANGELOG.md  

\*\*Goal:\*\* Deliver a fully functional CRM MVP with realistic data, validation, automation, and reporting (milestone reached at v1.4.3).

\---

\#\# Phase v1.5 (Enhanced MVP)

\*\*Tech:\*\* Google Sheets \+ Apps Script    
\*\*Focus:\*\* Marketable prototype, more automation & usability  

\*\*Key Features\*\*  
\- \*\*RBAC (Simulated):\*\* Protected ranges and branch/role-based filtered views    
\- \*\*Basic Audit Trail:\*\* Lightweight logging sheet (user, action, timestamp)  
\- \*\*Case & Revenue Module:\*\* Track cases, commission, and revenue attribution    
\- \*\*UT Dashboarding & Calculations Module:\*\* NAV, dividends, DCA, notifications    
\- \*\*Pseudo-APIs:\*\* Apps Script Web Apps endpoints to simulate integration points    
\- \*\*Separate Data vs Presentation Layer:\*\* Apps Script handles calculations; Sheets only store data/present    
\- \*\*Further Library Modularity:\*\* Refactor scripts into centralized, reusable library  

\*\*Deferred to v2.0:\*\*    
\- Advanced BI / Analytics integration (Tableau, Power BI)    
\- Advanced KPI dashboards tied to scalable backend

\*\*Goal:\*\* Provide a semi-market-ready prototype with richer functionality, modularity, and simulated integrations.

\---

\#\# Phase v2.0 (Full Stack Transition)

\*\*Tech:\*\* Python (FastAPI/Flask/Django), PostgreSQL/MySQL, React/Vue frontend    
\*\*Focus:\*\* Transition away from Google Sheets into a backend \+ scalable UI  

\*\*Key Features\*\*  
\- \*\*Backend Migration:\*\* Data moved to relational DB in 3NF    
\- \*\*Robust Security:\*\* Encryption at rest & in transit (AES-256, TLS), MFA    
\- \*\*Role-Based Access Control:\*\* Fine-grained permissions by role/customer    
\- \*\*Audit Logging:\*\* Programmatic immutable logs for all CRUD actions    
\- \*\*ETL Pipelines:\*\* Clean ingestion & validation of data from multiple sources    
\- \*\*Automated Retention Policies:\*\* Archive/delete data per regulations    
\- \*\*Workflow-driven Compliance:\*\* Automated KYC checks, basic alerts    
\- \*\*Web UI/UX Enhancement:\*\* Scalable frontend for RMs, Branch Managers, and Admins; improved usability & visualization    
\- \*\*Calendar-Based Appointment:\*\* Calendar module with scheduling integration and notifications    
\- \*\*Central Notification Module:\*\* Unified reminders/alerts across CRM modules    
\- \*\*Indexing:\*\* Database-level indexing for faster queries & scalability    
\- \*\*Analytics & KPIs (Advanced):\*\* Robust dashboards with advanced pipeline KPIs and BI integrations (Tableau / Power BI)  

\*\*Goal:\*\* Establish a production-ready, scalable architecture with robust auditability, notification systems, and a professional frontend.  

\---

\#\# Phase v3.0 (AI/ML – Intelligent CRM)

\*\*Tech:\*\* ML models, AI services, NLP integrations    
\*\*Focus:\*\* Proactive compliance, predictive analytics, intelligent assistant  

\*\*Architecture Layers\*\*  
\- \*\*Presentation Layer:\*\* Interactive dashboards with predictive insights, natural language query support    
\- \*\*Application Layer:\*\* ML-driven modules for lead scoring, churn prediction, portfolio recommendations    
\- \*\*Data Access Layer:\*\* Query optimization, caching with Redis, staging for analytics    
\- \*\*Data Layer:\*\* Hybrid OLTP (Postgres) \+ OLAP (Snowflake/BigQuery) with historical storage    
\- \*\*Integration Layer:\*\* External banking APIs, regulatory monitoring feeds, AI pipelines  

\*\*Key Features\*\*  
\- \*\*AI for Compliance & Risk:\*\* ML-based anomaly detection, AML/fraud flagging    
\- \*\*Predictive Analytics:\*\* Lead scoring, churn prediction    
\- \*\*Intelligent Consent Management:\*\* Automated opt-in/opt-out tracking    
\- \*\*Explainable AI:\*\* Transparent auditing of ML-based decisions    
\- \*\*Regulatory Monitoring:\*\* NLP-driven alerting on regulatory updates    
\- \*\*Advanced Data Governance:\*\* Automated discovery/classification of sensitive data  

\*\*Goal:\*\* Position the CRM as an intelligent, compliance-first solution; differentiate in the market

