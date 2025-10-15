\# User Acceptance Test (UAT) Plan

\#\# 1\. Introduction  
This UAT plan defines the testing approach to validate that the CRM MVP (v1.4.3) meets the agreed business requirements.    
The focus is on ensuring usability for Relationship Managers (RMs) and correctness of key workflows.  

\---

\#\# 2\. Scope  
\- \*\*In-Scope:\*\* Core CRM modules (Customer Management, Sales Funnel, Opportunity, Appointment, Staff Management, AUM Dashboard).    
\- \*\*Out-of-Scope:\*\* Advanced RBAC, external system integrations, predictive analytics, and compliance automation (planned for later phases).  

\---

\#\# 3\. Objectives  
\- Validate that the CRM MVP supports daily RM operations.    
\- Confirm that requirements defined in \*\*BRD.md\*\* and \*\*USERSTORY.md\*\* are satisfied.    
\- Ensure data integrity, validation rules, and calculated fields function as expected.  

\---

\#\# 4\. UAT Participants  
\- \*\*Primary Testers:\*\* Relationship Managers (pilot users).    
\- \*\*Observers:\*\* Branch Managers (for supervisory workflows).    
\- \*\*Developer/Analyst:\*\* Solo developer (for bug fixes and clarifications).  

\---

\#\# 5\. Test Environment  
\- Platform: \*\*Google Sheets \+ Apps Script (v1.4.3)\*\*    
\- Data: Realistic generated sample data (CIF, demographics, AUM, funnels, opportunities, appointments, staff).    
\- Access: Testers receive user copy of the CRM connected to library functions.  

\---

\#\# 6\. Test Scenarios

\#\#\# 6.1 Customer Management  
\- \*\*TC-01:\*\* Add a new customer record and confirm unique CIF is enforced.    
\- \*\*TC-02:\*\* Update customer demographics and verify AUM auto-recalculation.    
\- \*\*TC-03:\*\* Check Age Group and Risk Profile derived correctly.  

\#\#\# 6.2 Sales Funnel  
\- \*\*TC-04:\*\* Create a new funnel record for a customer and confirm Funnel\_ID uniqueness.    
\- \*\*TC-05:\*\* Update funnel engagement status and verify duration calculation.    
\- \*\*TC-06:\*\* Check stale contact highlighting after defined threshold.  

\#\#\# 6.3 Opportunity Management  
\- \*\*TC-07:\*\* Create an opportunity linked to customer and staff.    
\- \*\*TC-08:\*\* Update status and confirm probability color coding.    
\- \*\*TC-09:\*\* Verify Days-to-Close calculation works correctly.  

\#\#\# 6.4 Appointment Management  
\- \*\*TC-10:\*\* Schedule appointment linked to opportunity and confirm linkage.    
\- \*\*TC-11:\*\* Record appointment outcome and next action date.    
\- \*\*TC-12:\*\* Verify appointments not linked to opportunities (general meetings) are still valid.  

\#\#\# 6.5 Staff Management  
\- \*\*TC-13:\*\* Add a new RM and confirm unique Staff\_ID.    
\- \*\*TC-14:\*\* Assign RM to customer and validate mapping consistency.  

\#\#\# 6.6 AUM Dashboard  
\- \*\*TC-15:\*\* Check pivot tables and charts update correctly after new data.    
\- \*\*TC-16:\*\* Validate AUM bands, tiers, and portfolio distributions display correctly.  

\---

\#\# 7\. Acceptance Criteria  
\- All \*\*mandatory test cases (TC-01 to TC-16)\*\* pass with expected results.    
\- No critical defects remain unresolved.    
\- Data consistency and validation rules operate without error.    
\- RMs confirm usability and logical workflow alignment.  

\---

\#\# 8\. Deliverables  
\- Completed \*\*UAT results log\*\* with pass/fail status.    
\- Defect list with severity and resolution notes.    
\- Formal UAT sign-off from pilot testers.  

\---

\#\# 9\. Timeline  
\- \*\*Preparation:\*\* 1 week (environment setup, user briefing).    
\- \*\*Execution:\*\* 1 week (UAT execution, defect logging).    
\- \*\*Closure:\*\* 1-2 days (defect retest, sign-off).  

\---

\#\# 10\. Sign-Off  
UAT is considered complete when all test cases pass, critical issues are resolved, and stakeholders approve the solution for milestone release.  

