\# Process Flows (BPMN)

This document contains business process flows for the CRM MVP (up to v1.4.3).    
All diagrams are modeled in BPMN 2.0 using PlantUML syntax.

\---

\#\# 1\. Customer Onboarding

\`\`\`plantuml  
@startuml  
\!include \<bpmn\>

start  
:Collect Customer Info;  
:Validate Documents;  
diamond "Valid?" as valid  
yes \--\> :Assign RM;  
:Create Customer Record in CRM;  
stop

valid \--\> no  
:Request Missing Info;  
back to "Collect Customer Info"  
@enduml

\#\# 2\. Sales Funnel Management

@startuml  
\!include \<bpmn\>

start  
:Create Lead;  
:Qualify Lead;  
diamond "Qualified?" as q  
yes \--\> :Create Opportunity;  
:Update Funnel Stage;  
stop

q \--\> no  
:Mark as Lost;  
stop  
@enduml

\#\# 3\. Appointment Scheduling

@startuml  
\!include \<bpmn\>

start  
:RM Requests Appointment;  
:Send Request to Customer;  
diamond "Customer Confirms?" as c  
yes \--\> :Log Appointment in CRM;  
:Notify RM;  
stop

c \--\> no  
:Reschedule / Cancel;  
stop  
@enduml

\#\# 4\. Opportunity Closure

@startuml  
\!include \<bpmn\>

start  
:Update Opportunity Status;  
diamond "Won or Lost?" as w  
yes \--\> :Record Revenue / Commission;  
:Refresh Dashboard;  
stop

w \--\> no  
:Close as Lost;  
:Update Funnel Stage;  
stop  
@enduml

