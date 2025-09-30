\# USERSTORY.md

\#\# Overview  
This document captures the \*\*user stories\*\* for the v1.0.0 up to v1.4.0.    
They are structured in the format:  

\> \*\*As a \[role\], I want \[goal\], so that \[benefit\].\*\*

Each story includes \*\*acceptance criteria\*\* to define when it is considered done.  

\---

\#\# 1\. Customer Management

\#\#\# US-001: Capture customer profiles  
\- \*\*Story\*\*: As a Relationship Manager (RM), I want to record a new customer's demographic and product details, so that I have a single source of truth for customer data.    
\- \*\*Acceptance Criteria\*\*:    
  \- A new customer record can be added with a unique CIF.    
  \- Mandatory fields (CIF, IC, Name) must be validated.    
  \- Duplicate CIFs are not allowed.  

\#\#\# US-002: View customer portfolio  
\- \*\*Story\*\*: As an RM, I want to view a customer's AUM and product holdings, so that I can understand their portfolio at a glance.    
\- \*\*Acceptance Criteria\*\*:    
  \- AUM auto-calculates from CASA, FD, UT values.    
  \- Portfolio view shows balances and percentage distribution.  

\---

\#\# 2\. Sales Funnel

\#\#\# US-003: Track funnel stages  
\- \*\*Story\*\*: As an RM, I want to move leads through funnel stages (e.g., Contacted → Meeting → Proposal → Won/Lost), so that I can measure progress.    
\- \*\*Acceptance Criteria\*\*:    
  \- Funnel stages can be updated per customer-product opportunity.    
  \- Stage timestamps are recorded automatically.    
  \- A stale lead (30+ days in the same stage) is highlighted.  

\---

\#\# 3\. Opportunity Management

\#\#\# US-004: Record opportunities  
\- \*\*Story\*\*: As an RM, I want to log new opportunities with value, probability, and expected close date, so that I can forecast revenue.    
\- \*\*Acceptance Criteria\*\*:    
  \- Each opportunity is linked to a customer CIF and staff ID.    
  \- Days-to-close is calculated automatically.    
  \- Probability and status are dropdowns with controlled values.  

\---

\#\# 4\. Appointment Scheduling

\#\#\# US-005: Schedule appointments  
\- \*\*Story\*\*: As an RM, I want to schedule meetings and calls with customers, so that I can manage follow-ups effectively.    
\- \*\*Acceptance Criteria\*\*:    
  \- Appointment requires customer CIF and RM Staff ID.    
  \- Appointment type (call, meeting, virtual) is selectable.    
  \- Outcome and notes can be recorded after the appointment.  

\#\#\# US-006: Link appointments to opportunities  
\- \*\*Story\*\*: As an RM, I want to associate an appointment with an opportunity, so that I can track deal-related interactions.    
\- \*\*Acceptance Criteria\*\*:    
  \- Appointment record can link to an Opportunity ID.    
  \- Linked appointments display in the Opportunity view.  

\---

\#\# 5\. Staff Management

\#\#\# US-007: Manage staff directory  
\- \*\*Story\*\*: As an Admin, I want to maintain a list of staff with roles and branch mapping, so that CRM records are consistently assigned.    
\- \*\*Acceptance Criteria\*\*:    
  \- Staff ID is unique and mandatory.    
  \- Staff records include name, role, branch, region, status.    
  \- Inactive staff cannot be assigned to new opportunities.  

\---

\#\# 6\. Dashboards & Analytics

\#\#\# US-008: Monitor AUM distribution  
\- \*\*Story\*\*: As a Branch Manager, I want to see the distribution of AUM across CASA, FD, UT, so that I can assess portfolio balance.    
\- \*\*Acceptance Criteria\*\*:    
  \- AUM Dashboard shows total and segmented AUM.    
  \- Dashboard auto-updates when Customer\_Master changes.  

\#\#\# US-009: Track funnel conversion rates  
\- \*\*Story\*\*: As a Branch Manager, I want to see funnel conversion metrics across RMs, so that I can evaluate team performance.    
\- \*\*Acceptance Criteria\*\*:    
  \- Funnel dashboard shows conversions by stage.    
  \- Data can be filtered by RM or branch.  

\---

\#\# 7\. Data Quality & Validation

\#\#\# US-010: Data validation  
\- \*\*Story\*\*: As a System User, I want standardized drop-downs and validation rules, so that errors are minimized.    
\- \*\*Acceptance Criteria\*\*:    
  \- Lookup tables enforce controlled values.    
  \- Invalid inputs trigger warnings.    
  \- Email, phone number, and IC formats are validated.  

\---

\#\# Notes  
\- Covers scope up to \*\*MVP v1.4.0\*\*.  

