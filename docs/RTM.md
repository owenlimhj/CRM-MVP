\# Requirements Traceability Matrix (RTM)

\#\# Purpose  
This matrix ensures that all business requirements are covered by functional requirements, implemented in the CRM MVP, and validated through user stories and test cases.

\---

\#\# Legend  
\- \*\*BRD-ID\*\*: Business Requirement from BRD.md    
\- \*\*FR-ID\*\*: Functional Requirement (derived from BRD)    
\- \*\*US-ID\*\*: User Story from USERSTORY.md    
\- \*\*TC-ID\*\*: Test Case (planned for UAT)  

\---

\#\# Traceability Table

| BRD-ID | FR-ID | US-ID | TC-ID | Coverage Description |  
|--------|-------|-------|-------|-----------------------|  
| BR-01 Centralize customer information | FR-01 Customer\_Master captures unique demographics & AUM | US-01 RM creates a new customer record | TC-01 Verify RM can create customer with valid CIF and no duplicates |  
| BR-02 Manage pipelines efficiently | FR-02 Sales\_Funnel tracks funnel stages | US-02 RM moves customer through funnel stages | TC-02 Verify funnel stages update and stale contacts are highlighted |  
| BR-03 Track opportunities | FR-03 Opportunity sheet records product, value, probability, status | US-03 RM logs a new opportunity | TC-03 Verify opportunity auto-links to customer and updates dashboard |  
| BR-04 Appointment management | FR-04 Appointment sheet logs activity, outcome, follow-ups | US-04 RM schedules an appointment | TC-04 Verify appointment is saved, overdue items highlighted |  
| BR-05 Staff-role mapping | FR-05 Staff\_Master maintains staff, role, branch | US-05 RM/Manager views staff assignments | TC-05 Verify staff records validate against customers/opportunities |  
| BR-06 Portfolio monitoring | FR-06 AUM\_Dashboard provides portfolio insights | US-06 Manager views AUM dashboard | TC-06 Verify dashboard aggregates AUM by product, tier, RM |  
| BR-07 Data quality & validation | FR-07 Lookups enforce controlled values (roles, tiers, segments) | US-07 RM enters data using dropdowns | TC-07 Verify invalid email/phone formats are rejected |  
| BR-08 Compliance readiness (future) | FR-08 Baseline protections, version history for audit | US-08 RM data entries are logged in Sheets version history | TC-08 Verify changes visible in version history (interim audit trail) |

\---

\#\# Notes  
\- Coverage is complete for MVP v1.4.3 scope.    
\- Advanced features (RBAC, Audit Trail, Case Module, UT Dashboard) will be mapped in \*\*RTM v1.5 update\*\*.    
\- Test Cases (TC-XX) are placeholders for UAT planning — not all scripts are developed yet.  

