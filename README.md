
# Healthcare EIS with Power Bi

In this Power BI project, we use 9 fail-proof business analysis/intelligence processes to craft a top-notch dashboard 
using NTPF data from Group Hospital, which is essentially an aggregation of Inpatient, Day Case, and Outpatient waiting
lists for comprehensive insights.



### Dashboard Link: 
* The initial report was published to this power bi workspace and available on request, however, a copy of the dashboard
    is included in the project repository.

    [https://app.powerbi.com/groups/me/reports/789d1154-8dd7-4307-b6b3-84e6251ed2f3/ReportSection?experience=power-bi]()

#

### Data Sources and Information:
The data used in this project was taken from:

* Outpatient: [https://data.world/ie-nat-purchase-fund/b497f818-a078-449e-b992-2828fe814230]()

* Inpatient: [https://data.world/ie-nat-purchase-fund/a8352e39-3fbb-4b06-9921-96e54e0be187]()


### **Data Dictionary**

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



### **Summary Notes for Patient Waiting Lists:**

##### Outpatient

1. Responsibility and Reporting:
   - The National Treatment Purchase Fund (NTPF) manages the collection, collation, and validation of Inpatient, Day Case, and Outpatient waiting lists.
   - The Outpatient (OP) Waiting List report focuses on the total number of patients waiting for a first appointment at a consultant-led Outpatient clinic, categorized across various time bands.
2. Confidentiality Measures:
   - Numbers under a 'Small Volume' heading aggregate counts where there are fewer than 5 patients waiting in a particular specialty/hospital for confidentiality.
3. Data Classification:
   - Adult/Child classification is based on each hospital's designation, with specific criteria for Children's Hospitals, Adult-only hospitals, and mixed Adult/Child hospitals.
4. Data Collection and Publication:
   - NTPF captures a snapshot of the number of patients waiting in each hospital, publishing the aggregated data monthly on their website.
5. Responsibility and Quality Assurance:
   - Boards and management of individual public hospitals are responsible for the accuracy and integrity of patient data submitted to NTPF.
   - Continuous collaboration between NTPF and individual hospitals addresses ongoing work on data quality, and technical and administrative issues are resolved as they arise.
6. Notes for Consideration:
   - Kilcreene Orthopaedic - OP waiting list included with St Luke’s Hospital Kilkenny.
   - Tallaght Paediatrics and Adults figures are shown separately from July 2015.
   - PAS system upgrade impacted data submission from University Hospital Limerick in July 2015, resolved by September 2015.
   - Rotunda hospital included in reporting from January 2018.
   - PAS system upgrade in Nenagh Hospital resulted in no file received for October 2016 publication.

##### Inpatient and Day Care

1. **Responsibility and Reporting:**
   - The National Treatment Purchase Fund (NTPF) manages the collection, collation, and validation of Inpatient, Day Case, and Outpatient waiting lists.
   - The Inpatient and Day Case (IPDC) Waiting List report details the total number of patients awaiting Inpatient and Day Case treatment across various time bands within each Specialty.
2. **Confidentiality Measures:**
   - Numbers under a 'Small Volume' heading aggregate counts where there are fewer than 5 patients waiting in a particular specialty/hospital to preserve confidentiality.
3. **Data Classification:**
   - Adult/Child classification is based on each hospital's designation, with specific criteria for Children's Hospitals, Adult-only hospitals, and mixed Adult/Child hospitals.
4. **Data Collection and Publication:**
   - NTPF captures a snapshot of the number of patients waiting in each hospital, publishing the aggregated data monthly on their website.
5. **Responsibility and Quality Assurance:**
   - Boards and management of individual public hospitals are responsible for the accuracy and integrity of patient data submitted to NTPF.
   - Continuous collaboration between NTPF and individual hospitals addresses ongoing work on data quality, and technical and administrative issues are resolved as they arise.
6. **Notes for Consideration:**
   - Time band categories on reports were standardized from January 2018, aligning with DoH/HSE clearance targets for waiting lists.
   - Specific updates for hospitals like St. Michaels, Dun Laoghaire, and Tallaght Paediatrics and Adults figures are provided.
   - System upgrades in University Hospital Limerick, St John's Hospital Limerick, and Nenagh Hospital affected data submission during certain periods.
#

## Problem Statement
The current issue revolves around inefficiencies in maintaining and extracting insights from patient waiting list data
at Group Hospital. Currently, there is a lack of a comprehensive and user-friendly system for monitoring real-time 
waiting list statuses, and available specialties, as well as the capacity for analyzing historical patterns in 
inpatient and outpatient categories and doing thorough specialty-level and age profile assessments. Stakeholders 
suffer from an absence of a centralized and visually intuitive solution, which limits their capacity to make informed 
choices promptly. 

#


### The 9-BA/BI Steps For Dashboard Development

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
#### 1. Requirement gathering
This is the most important step of dashboard creation. The effectiveness of your dashboard/report is determined by its 
capacity to address the specific business need/problem, not by its visual attractiveness. So, by gathering the needs for
your dashboard, you may make better use of your time by producing what is required.
This article describes four consecutive steps for gathering the requirements for your dashboard/reports, so you can offer
value to your stakeholders.



- **Identify Stakeholders:**

Determine the primary stakeholders and establish a point of contact, such as domain experts or leaders who will utilize the dashboard.
Setting a point of contact at the outset is crucial for seeking explanations and clarifications as needed. For this 
particular project, the stakeholders are Hospital Administrators, Department Heads, Medical Staff, Data Analysts/IT 
Department, Quality Assurance Team, Patients, Government Health Agencies, and Hospital Board Members.

- **Understand Business Objectives:**

Having identified your stakeholders, the next step is to engage in meetings and calls with stakeholders to obtain a
comprehensive outline of goals for the entire endeavor. This will include setting up meetings via skype, google meet, team
meeting etc depending on the type of organization and the tools they use for collaboration. You have to ask open-ended 
questions during these discussions aids in gaining deeper insights into the data and understanding how the dashboard 
aligns with specific business goals. From the problem statement, we identify 3 key objectives:
 * Track the current status of patients' waiting lists.
 * Analyze historical monthly trends for inpatient and outpatient categories.
 * Perform detailed specialty-level and age profile analyses.

- **High-Level Data Study:**

Conduct a high-level overview of the data, focusing on key aspects without delving into detailed analysis.
Topics to cover include data source, column descriptions, data types, volume, frequency, and data quality (identifying missing values or anomalies).

- **Define Scope:**

Engage in discussions with stakeholders to define the scope, discussing key metrics, KPIs, and deployment timelines.
Document calculations, timeframes, and scope details during this stage to set clear expectations and avoid future disagreements.

###### TIP: Follow 80-20 Rule:
When estimating your ETA, as a best practice, adhere to the 80-20 rule, keeping a 20% buffer while finalizing deadlines.
This ensures a margin for over-delivering beyond standard commitments and mitigates the risk of falling short after an initially extraordinary pitch.



### Data Collection
### Data Transformation and Modeling
### Data Visualization Blueprint
### Dashboard Layout and Design
### Interactivity and Navigation
### Testing
### Sharing
### Maintenance and Refresh.


#
Title and KPI Visuals
![image](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/eba8a737-caaa-4577-b528-5b02c768adf9)

#
Key Performance Indicators (Average/Median WaitList, Age Groups, and Specialty Name):

![image](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/af36b053-3476-40c8-b30c-fc8756a53dd2)


#
Monthly Trend Analysis:

![Trend analysis](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/96496d11-9831-409e-9692-7679dd826936)

#
Detailed Analysis:

![image](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/24b0512d-4519-426e-b008-9c156df7e8e6)


#



