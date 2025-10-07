\# Business Requirements Document (BRD) – v1.1.0

\#\# 1\. Project Overview  
The CRM MVP is designed to support Relationship Managers (RMs) in banking by providing a lightweight and structured tool for managing customers and basic sales funnel tracking.  

This version (v1.1.0) establishes the \*\*foundation\*\*: centralizing customer information, introducing funnel tracking, and enabling basic AUM insights.  

\---

\#\# 2\. Objectives  
\- Create a \*\*single source of truth\*\* for customer and portfolio data.    
\- Provide RMs with visibility into \*\*customer tiers and product holdings\*\*.    
\- Introduce \*\*Sales Funnel\*\* tracking for early-stage opportunity management.  

\---

\#\# 3\. Scope (v1.0 – v1.1)  
\- \*\*Customer Management\*\*: Demographics, AUM, tiering.    
\- \*\*Sales Funnel Tracking\*\*: Engagement status and notes.    
\- \*\*Dashboard (Basic)\*\*: AUM bands by customer tier.    
\- \*\*Sample Data Generation\*\*: Placeholder CIFs, demographics, products.  

\---

\#\# 4\. Stakeholders  
\- \*\*Primary Users\*\*: Relationship Managers (RMs).    
\- \*\*Secondary Users\*\*: Branch Managers.    
\- \*\*Project Owner\*\*: Solo developer (portfolio project).  

\# Business Requirements Document (BRD) – v1.3.0

\#\# 1\. Project Overview  
By v1.3.0, the CRM MVP evolves from a static foundation into a governed, automated structure.    
This release introduces \*\*data validation, lookup controls, automation, and conditional formatting\*\* to enforce data quality and reduce manual work.  

\---

\#\# 2\. Objectives  
\- Enforce \*\*data governance\*\* through validations and lookup tables.    
\- Automate \*\*AUM calculations\*\* and product consistency checks.    
\- Improve \*\*usability and error prevention\*\* with conditional formatting.  

\---

\#\# 3\. Scope (v1.2 – v1.3)  
\- \*\*Data Validation & Lookups\*\*: Centralized reference tables.    
\- \*\*Automation\*\*: Auto-calculated AUM, tier, and banding.    
\- \*\*Conditional Formatting\*\*: Color scales for key metrics, staleness flags.    
\- \*\*Sales Funnel Enhancements\*\*: Basic duration tracking.  

\---

\#\# 4\. Non-Functional Requirements  
\- \*\*Data Quality\*\*: Structured entry enforced via validation.    
\- \*\*Usability\*\*: Drop-downs, formatting cues, reduced error risk.  

\---

\#\# 5\. Success Criteria  
\- RMs can manage \*\*100+ customers\*\* with consistent, error-free records.    
\- AUM, Tier, and Funnel metrics \*\*auto-update\*\* without manual recalculation.  

# Business Requirements Document (BRD) – v1.4.0

## 1. Project Overview
At v1.4.0, the CRM MVP moves from governed sheets into a **relational-like design** with multiple linked modules.  
This release adds **Opportunity, Appointment, and Staff_Master** tables, creating the backbone for a more complete CRM workflow.  

---

## 2. Objectives
- Expand CRM into a **multi-sheet relational flow**.  
- Support **opportunity management** and deal tracking.  
- Enable **appointment scheduling** linked to customers/opportunities.  
- Introduce **staff allocation** for RM mapping and oversight.  

---

## 3. Scope (v1.4.0)
- **Customer_Master**: Expanded with contact info, segments, risk profiles.  
- **Opportunity**: Deal-level tracking with probability and days-to-close.  
- **Appointment**: Meetings, outcomes, linked to opportunities.  
- **Staff_Master**: RM details, branch, role, status.  
- **Dashboards**: AUM pivot, pipeline conversion metrics.  

---

## 4. Non-Functional Requirements
- **Portability**: Still Google Sheets, but structured for SQL migration.  
- **Scalability**: Normalized schema with relational references.  

---

## 5. Roadmap
- Next release (Enhanced MVP v1.5): **Audit trail, RBAC, UT dashboards, pseudo-APIs.**  
- Long-term (v2.0): **Full-stack CRM with backend + compliance modules.**  
