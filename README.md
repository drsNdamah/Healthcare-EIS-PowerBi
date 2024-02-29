
# Healthcare EIS with Power Bi

In this Power BI project, we go through 9 fail-proof business analysis processes to craft a top-notch dashboard using NTPF hospital data, aggregating Inpatient, Day Case, and Outpatient waiting lists for comprehensive insights.

### Dashboard Link: https://app.powerbi.com/groups/me/reports/789d1154-8dd7-4307-b6b3-84e6251ed2f3/ReportSection?experience=power-bi

## Problem Statement
The current issue revolves around inefficiencies in maintaining and extracting insights from patient waiting list data at Group Hospital. Currently, there is a lack of a comprehensive and user-friendly system for monitoring real-time waiting list statuses, and available specialties, as well as the capacity for analyzing historical patterns in inpatient and outpatient categories and doing thorough specialty-level and age profile assessments. Stakeholders suffer from an absence of a centralized and visually intuitive solution, which limits their capacity to make informed choices promptly. 

### The 9-BA/BI fail-proof Steps followed

To address these challenges, the project will follow a meticulous nine-step BA/BI dashboard/report development process, including:

* requirement gathering, 
* data collection,
* data transformation and modeling,
* data visualization blueprint,
* dashboard layout and design,
* interactivity and navigation,
* testing, 
* sharing,
* maintenance and refresh.


### Steps/Processes in Details
#### Requirement gathering

* Identify Stakeholders:

Determine the primary stakeholders and establish a point of contact, such as domain experts or leaders who will utilize the dashboard.
Setting a point of contact at the outset is crucial for seeking explanations and clarifications as needed.

* Understand Business Objectives:
Engage in meetings and calls with stakeholders to obtain a comprehensive outline of goals for the entire endeavor.
Asking open-ended questions during these discussions aids in gaining deeper insights into the data and understanding how the dashboard aligns with specific business goals.

* High-Level Data Study:
Conduct a high-level overview of the data, focusing on key aspects without delving into detailed analysis.
Topics to cover include data source, column descriptions, data types, volume, frequency, and data quality (identifying missing values or anomalies).

* Define Scope:
Engage in discussions with stakeholders to define the scope, discussing key metrics, KPIs, and deployment timelines.
Document calculations, timeframes, and scope details during this stage to set clear expectations and avoid future disagreements.

* Follow 80-20 Rule:
As a best practice, adhere to the 80-20 rule, keeping a 20% buffer while finalizing deadlines.
This ensures a margin for over-delivering beyond standard commitments and mitigates the risk of falling short after an initially extraordinary pitch.



### Data Collection
### Data Transformation and Modeling
### Data Visualization Blueprint
### Dashboard Layout and Design
### Interactivity and Navigation
### Testing
### Sharing
### Maintenance and Refresh.


### Data Sources:

Outpatient: https://data.world/ie-nat-purchase-fund/b497f818-a078-449e-b992-2828fe814230

Inpatient: https://data.world/ie-nat-purchase-fund/a8352e39-3fbb-4b06-9921-96e54e0be187


### Data Dictionary

| Column Name          | Type    |
|----------------------|---------|
| archive_date         | date    |
| group                | string  |
| hospital_hipe        | integer |
| hospital             | string  |
| specialty_hipe       | integer |
| specialty            | string  |
| case_type            | string  |
| adult_child          | string  |
| age_categorization   | string  |
| time_bands           | string  |
| count                | integer |

#

**Summary Notes for Inpatient (IPDC) Waiting Lists:**

- **Responsibility and Reporting:**
  - The National Treatment Purchase Fund (NTPF) manages the collection, collation, and validation of Inpatient, Day Case, and Outpatient waiting lists.
  - The Inpatient and Day Case (IPDC) Waiting List report details the total number of patients awaiting Inpatient and Day Case treatment across various time bands within each Specialty.

- **Confidentiality Measures:**
  - Numbers under a 'Small Volume' heading aggregate counts where there are fewer than 5 patients waiting in a particular specialty/hospital to preserve confidentiality.

- **Data Classification:**
  - Adult/Child classification is based on each hospital's designation, with specific criteria for Children's Hospitals, Adult-only hospitals, and mixed Adult/Child hospitals.

- **Data Collection and Publication:**
  - NTPF captures a snapshot of the number of patients waiting in each hospital, publishing the aggregated data monthly on their website.

- **Responsibility and Quality Assurance:**
  - Boards and management of individual public hospitals are responsible for the accuracy and integrity of patient data submitted to NTPF.
  - Continuous collaboration between NTPF and individual hospitals addresses ongoing work on data quality, and technical and administrative issues are resolved as they arise.

- **Notes for Consideration:**
  - Time band categories on reports were standardized from August 2015, aligning with DoH/HSE clearance targets for waiting lists.
  - Specific updates for hospitals like St. Michaels, Dun Laoghaire, and Tallaght Paediatrics and Adults figures are provided.
  - System upgrades in University Hospital Limerick, St John's Hospital Limerick, and Nenagh Hospital affected data submission during certain periods.


#

**Summary Notes for Outpatient (OP) Waiting Lists:**

- **Responsibility and Reporting:**
  - The National Treatment Purchase Fund (NTPF) manages the collection, collation, and validation of Inpatient, Day Case, and Outpatient waiting lists.
  - The Outpatient (OP) Waiting List report focuses on the total number of patients waiting for a first appointment at a consultant-led Outpatient clinic, categorized across various time bands.

- **Confidentiality Measures:**
  - Numbers under a 'Small Volume' heading aggregate counts where there are fewer than 5 patients waiting in a particular specialty/hospital for confidentiality.

- **Data Classification:**
  - Adult/Child classification is based on each hospital's designation, with specific criteria for Children's Hospitals, Adult-only hospitals, and mixed Adult/Child hospitals.

- **Data Collection and Publication:**
  - NTPF captures a snapshot of the number of patients waiting in each hospital, publishing the aggregated data monthly on their website.

- **Responsibility and Quality Assurance:**
  - Boards and management of individual public hospitals are responsible for the accuracy and integrity of patient data submitted to NTPF.
  - Continuous collaboration between NTPF and individual hospitals addresses ongoing work on data quality, and technical and administrative issues are resolved as they arise.

- **Notes for Consideration:**
  - Kilcreene Orthopaedic - OP waiting list included with St Luke’s Hospital Kilkenny.
  - Tallaght Paediatrics and Adults figures are shown separately from July 2015.
  - PAS system upgrade impacted data submission from University Hospital Limerick in July 2015, resolved by September 2015.
  - Rotunda hospital included in reporting from August 2015.
  - PAS system upgrade in Nenagh Hospital resulted in no file received for October 2016 publication.


![image](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/af36b053-3476-40c8-b30c-fc8756a53dd2)


#
Monthly Trend Analysis:

![Trend analysis](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/96496d11-9831-409e-9692-7679dd826936)

