# CRM Project Changelog

All notable changes to this project are documented here.  
This project started as a solo MVP in Google Sheets and evolved iteratively.

---

## [v1.0.0]
### Added
- Created **initial MVP skeleton** with following sheets:
  - `Customer_Master`, `Sales_Funnel`, `AUM_Dashboard`
- Added initial columns:
  - **Customer_Master:** CIF, IC, Name, Age, Tier, Branch Code, RM Code, Region, AUM Band, Risk Profile, Product Holding, CASA, FD, UT, SP, Banca, CC
  - **Sales_Funnel:** CIF, Name, Contact No, Status, Last Contacted, Notes
- Implemented first **Apps Script** to generate placeholder sample data for `Customer_Master` (CIF & Region)

---

## [v1.1.0]
### Changed
- Refined **Customer_Master schema**:
  - Added `Age Group`, `Gender`, `AUM`, `Online Banking`
  - Adjusted column ordering for logical grouping
- Improved **sample data generation**:
  - Generated realistic sample data across all columns
  - Introduced constraints for **Customer ID & Demographics**:
    - Unique CIFs & ICs (Malaysia & Singapore formats)
    - Age derived realistically from IC
    - Gender derived from IC (MY) or randomized (SG)
    - Realistic names by ethnic diversity & gender
    - Realistic phone numbers with country-specific prefixes
    - Age Group segmentation
  - Introduced **Portfolio & Financial constraints**:
    - Random but realistic CASA, FD, UT, SP, Banca holdings
    - Age-based wealth distribution, zero-product probability
    - AUM & AUM Band calculation, Tiering logic
    - Risk profile & online banking adoption logic

---

## [v1.2.0]
### Added
- **Data Validation & Lookups:**
  - Centralized `Lookups` sheet for reusable drop-downs
  - Validation for Age Group, Gender, Region, Tier, Risk Profile, Online Banking
  - Generated sample data for `Sales_Funnel`
- **Automation:**
  - Automated AUM calculation via formulas
- **Improved robustness:**
  - Removed hard-coded dependencies in Apps Script for flexibility
  - Validation rules made standalone & more robust

---

## [v1.3.0]
### Added
- Column filters for all `Customer_Master` columns
- Conditional formatting in `Customer_Master`:
  - Age Group: color scale
  - UT, SP, Banca, CC: highlight if zero
  - AUM, Tier: color scale
  - Online Banking: highlight if "No"

---

## [v1.4.0]
### Changed
- Reimagined **CRM flow & normalized schema**:  
  `Staff_Master` → `Customer_Master` → `Sales_Funnel` → `Opportunity` → `Appointment`
- Added **Staff_Master**, **Opportunity**, **Appointment** sheets
  - **Staff_Master:** Staff ID, Name, Role, Branch, Region, Status
  - **Opportunity:** Opty ID, Creation Date, CIF, Customer Name, Staff ID, Opty Status, Product Type, Sales Volume, Probability, Expected Close Date, Days to Close, Last Activity Date, Notes
  - **Appointment:** Appt ID, Opty ID, CIF, Name, Staff ID, Product Type, Appt Date/Time, Outcome
- Updated **Customer_Master schema**:
  - Added `Contact No`, `Email`, `Segment`, `Bond`, `Risk Profile Last Updated`
- Updated **Sales_Funnel schema**:
  - Added `Funnel ID`, `RM Staff ID`, Engagement Status fields
- Expanded **Lookups**: Roles, Segments, Engagement Status, Opty Status, Product Types
- Implemented **validation, conditional formatting & calculations across all sheets**:
  - Status highlights, staleness alerts, probability color scales, date constraints, etc.

—--
