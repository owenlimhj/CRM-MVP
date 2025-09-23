\# CRM Project Changelog

All notable changes to this project are documented here.    
This project started as a solo MVP in Google Sheets and evolved iteratively.

\---

\#\# \[v1.0.0\]  
\#\#\# Added  
\- Created \*\*initial MVP skeleton\*\* with following sheets:  
  \- \`Customer\_Master\`, \`Sales\_Funnel\`  
\- Added initial columns:  
  \- \*\*Customer\_Master:\*\* CIF, IC, Name, Age, Tier, Branch Code, RM Code, Region, AUM Band, Risk Profile, Product Holding, CASA, FD, UT, SP, Banca, CC  
  \- \*\*Sales\_Funnel:\*\* CIF, Name, Contact No, Status, Last Contacted, Notes  
\- Implemented first \*\*Apps Script\*\* to generate placeholder sample data for \`Customer\_Master\` (CIF & Region)

\---

\#\# \[v1.1.0\]  
\#\#\# Changed  
\- Refined \*\*Customer\_Master schema\*\*:  
  \- Added \`Age Group\`, \`Gender\`, \`AUM\`, \`Online Banking\`  
  \- Adjusted column ordering for logical grouping  
\- Improved \*\*sample data generation\*\*:  
  \- Generated realistic sample data across all columns  
  \- Introduced constraints for \*\*Customer ID & Demographics\*\*:  
    \- Unique CIFs & ICs (Malaysia & Singapore formats)  
    \- Age derived realistically from IC  
    \- Gender derived from IC (MY) or randomized (SG)  
    \- Realistic names by ethnic diversity & gender  
    \- Realistic phone numbers with country-specific prefixes  
    \- Age Group segmentation  
  \- Introduced \*\*Portfolio & Financial constraints\*\*:  
    \- Random but realistic CASA, FD, UT, SP, Banca holdings  
    \- Age-based wealth distribution, zero-product probability  
    \- AUM & AUM Band calculation, Tiering logic  
    \- Risk profile & online banking adoption logic