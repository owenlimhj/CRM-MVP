\# CRM MVP — Entity Relationship Diagram (ERD)

This ERD represents the logical relationships between the key sheets/tables in the CRM MVP.  
Use the Mermaid diagram below (GitHub renders Mermaid) and the field list for exact PK / FK mappings.

\---

\#\# Mermaid ERD

\`\`\`mermaid  
erDiagram  
  %% Entities  
  CUSTOMER\_MASTER {  
    string CIF PK "Customer Identifier"  
    string IC\_Number  
    string Name  
    number Age  
    string Age\_Group  
    string Gender  
    string Contact\_No  
    string Email  
    string Segment  
    string Branch\_Code  
    string Region  
    string RM\_Staff\_ID FK "-\> STAFF\_MASTER.Staff\_ID"  
    number CASA  
    number FD  
    number UT  
    number Bancassurance  
    number Bond  
    number AUM  
    string AUM\_Band  
    string Tier  
    string Risk\_Profile  
    date Risk\_Profile\_Last\_Updated  
    string Online\_Banking  
  }

  STAFF\_MASTER {  
    string Staff\_ID PK  
    string Staff\_Name  
    string Role  
    string Branch\_Code  
    string Region  
    string Status  
  }

  SALES\_FUNNEL {  
    string Funnel\_ID PK  
    string CIF FK "-\> CUSTOMER\_MASTER.CIF"  
    string Opty\_ID FK "-\> OPPORTUNITY.Opty\_ID"  
    string RM\_Staff\_ID FK "-\> STAFF\_MASTER.Staff\_ID"  
    string Stage  
    string Product\_Discussed  
    string Appointment\_Status  
    date Last\_Contacted  
    number Duration "days in funnel"  
  }

  OPPORTUNITY {  
    string Opty\_ID PK  
    date Creation\_Date  
    string CIF FK "-\> CUSTOMER\_MASTER.CIF"  
    string Customer\_Name  
    string RM\_Staff\_ID FK "-\> STAFF\_MASTER.Staff\_ID"  
    string Opty\_Status  
    string Product\_Type  
    number Sales\_Volume  
    number Probability  
    date Expected\_Close\_Date  
    number Days\_to\_Close  
    date Last\_Activity\_Date  
  }

  APPOINTMENT {  
    string Appt\_ID PK  
    string Opty\_ID FK "-\> OPPORTUNITY.Opty\_ID (nullable)"  
    string CIF FK "-\> CUSTOMER\_MASTER.CIF"  
    string Customer\_Name  
    string Staff\_ID FK "-\> STAFF\_MASTER.Staff\_ID"  
    string Product\_Discussed  
    datetime Appt\_DateTime  
    string Appt\_Type  
    string Activity\_Type  
    string Appointment\_Status  
    string Outcome  
    date Next\_Action\_Date  
  }

  LOOKUPS {  
    string Key PK  
    string Value  
    string Category  
  }

  %% Relationships  
  CUSTOMER\_MASTER ||--o{ SALES\_FUNNEL : "1..\*"  
  CUSTOMER\_MASTER ||--o{ OPPORTUNITY : "1..\*"  
  CUSTOMER\_MASTER ||--o{ APPOINTMENT : "1..\*"

  STAFF\_MASTER ||--o{ CUSTOMER\_MASTER : "1..\* (RM assignment)"  
  STAFF\_MASTER ||--o{ SALES\_FUNNEL : "1..\*"  
  STAFF\_MASTER ||--o{ OPPORTUNITY : "1..\*"  
  STAFF\_MASTER ||--o{ APPOINTMENT : "1..\*"

  SALES\_FUNNEL }o--|| OPPORTUNITY : "0..1 \-\> converted"  
  OPPORTUNITY ||--o{ APPOINTMENT : "0..\*"  
  LOOKUPS ||--o{ CUSTOMER\_MASTER : "n"  
  LOOKUPS ||--o{ SALES\_FUNNEL : "n"  
  LOOKUPS ||--o{ OPPORTUNITY : "n"  
  LOOKUPS ||--o{ APPOINTMENT : "n"

