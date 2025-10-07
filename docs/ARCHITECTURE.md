\# CRM MVP – System Architecture

\#\# 1\. Overview  
The CRM MVP is designed as a modular Google Sheets \+ Apps Script solution to unify customer data, sales funnel tracking, opportunity pipeline management, appointment scheduling, staff mapping, and portfolio dashboards.  

The system leverages lookup tables for controlled data consistency, conditional formatting for visual cues, and Apps Script libraries for reusable logic. It is built with scalability in mind, transitioning toward SQL, backend services, and BI integration in future versions.

\---

\#\# 2\. Architecture Layers

\- \*\*Presentation Layer\*\*    
  \- Google Sheets interface with dropdowns, validations, and conditional formatting.    
  \- Dashboards (e.g., \*\*AUM\_Dashboard\*\*) built with pivot tables and charts.  

\- \*\*Data Layer\*\*    
  \- Core sheets store structured records: \`Customer\_Master\`, \`Sales\_Funnel\`, \`Opportunity\`, \`Appointment\`, \`Staff\_Master\`, \`Lookups\`.    
  \- Validation rules (email, phone, duplicates, AUM consistency) ensure integrity.  

\- \*\*Logic Layer\*\*    
  \- Apps Script functions handle:    
    \- Data generation (sample realistic datasets).    
    \- Calculations (AUM rollups, pipeline metrics).    
    \- Validation & automation (stale contact checks, overdue highlights).    
  \- Library modularity allows reusability across “master” and “user” copies.  

\- \*\*Integration Layer\*\*    
  \- None in v1.4.3 (self-contained).    
  \- \*\*Planned (v1.5+):\*\* Pseudo-APIs with Apps Script Web Apps, Tableau/Power BI connectors.

\---

\#\# 3\. Core Modules

\- \*\*Customer\_Master\*\*    
  Central repository for customer demographics, contact info, segmentation, AUM, and RM mapping.  

\- \*\*Sales\_Funnel\*\*    
  Tracks engagement stages, ownership, status, and last-contacted dates.  

\- \*\*Opportunity\*\*    
  Records potential deals: product, value, probability, expected close date, and RM ownership.  

\- \*\*Appointment\*\*    
  Logs customer meetings, activity type, outcomes, and follow-ups. Linked to Customer\_Master and Opportunity.  

\- \*\*Staff\_Master\*\*    
  Registry of staff with IDs, names, branches, roles, and status (active/inactive).  

\- \*\*Lookups\*\*    
  Centralized reference values (roles, region, segment, product, tier, activity type).  

\- \*\*AUM\_Dashboard\*\*    
  Pivot-driven visualization of portfolio breakdown (CASA, FD, UT, SP, Bond, Banca, CC).  

\---

\#\# 4\. Data Flow

1\. \*\*Staff\_Master\*\* defines staff and branches.    
2\. Customers onboarded in \*\*Customer\_Master\*\*, linked to staff.    
3\. Leads tracked in \*\*Sales\_Funnel\*\* with RM mapping.    
4\. Converted into \*\*Opportunities\*\* for deal-level tracking.    
5\. Customer interactions logged in \*\*Appointment\*\*, tied back to CIF and Opportunity.    
6\. \*\*AUM\_Dashboard\*\* aggregates product balances for insights.    
7\. \*\*Lookups\*\* ensure consistency across all modules.  

\---

\#\# 5\. Relationships

\- \*\*Staff\_Master → Customer\_Master\*\*: Staff ID mapping.    
\- \*\*Customer\_Master → Sales\_Funnel\*\*: CIF linkage.    
\- \*\*Customer\_Master → Opportunity\*\*: CIF and staff mapping.    
\- \*\*Customer\_Master → Appointment\*\*: CIF linkage.    
\- \*\*Sales\_Funnel → Opportunity\*\*: Funnel conversion into opportunities.    
\- \*\*Appointment → Opportunity\*\*: Engagements tied to deals.  

\---

\#\# 6\. Documentation Links

\- \[ERD (PlantUML)\](./ERD.puml) – Entity relationships across modules.    
\- \[BRD\](./BRD.md) – Business requirements and scope.    
\- \[USERSTORY\](./USERSTORY.md) – End-user needs and acceptance criteria.    
\- \[UAT\_PLAN\](./UAT\_PLAN.md) – Test cases and validation approach.    
\- \[Process Flows\](./PROCESS\_FLOWS.md) – BPMN workflows.    
\- \[Changelog\](./CHANGELOG.md) – Iterative updates (latest: v1.4.3 milestone).    
\- \[Roadmap\](./ROADMAP.md) – Vision, layered evolution plan.  

\---

\#\# 7\. Scalability Notes

\- \*\*v1.0 – v1.4.3 (Current):\*\* Google Sheets \+ Apps Script, modular structure, reusable libraries, validation, realistic dataset generation, AUM Dashboard complete.    
\- \*\*v1.5 (Planned):\*\* Role-based access (simulated), audit trail, case & revenue module, UT dashboarding/calculations, pseudo-APIs, further modularity.    
\- \*\*v2.0 (Planned):\*\* SQL backend, Python API layer, secure role-based access, advanced audit logging, centralized notification system.    
\- \*\*v3.0 (Planned):\*\* AI/ML insights, predictive analytics, compliance automation.  

