
## **Healthcare EIS with Power Bi**

In this Power BI project, I follow 9 proven business analysis or intelligence processes to craft a top-notch Health EIS dashboard using NTPF data from Group Hospital, which is essentially an aggregation of Inpatient, Day Case, and Outpatient waiting lists for comprehensive insights.




### **Dashboard Links:**
The initial report was published to my personal power bi workspace and available on request, however, a copy of the dashboard (.pbix) is included in the project repository. You can request access to the report via:

[https://app.powerbi.com/groups/me/reports/789d1154-8dd7-4307-b6b3-84e6251ed2f3/ReportSection?experience=power-bi]()


### **Data Sources and Information:**
The data used in this project was taken from:

* Outpatient: [https://data.world/ie-nat-purchase-fund/b497f818-a078-449e-b992-2828fe814230]()

* Inpatient: [https://data.world/ie-nat-purchase-fund/a8352e39-3fbb-4b06-9921-96e54e0be187]()


#### **Data Dictionary:**
The following shows the description of the data used in this project by column name and datatype:

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

#### **Summary Notes for Patient Waiting Lists:**

The National Treatment Purchase Fund (NTPF) oversees the management of Inpatient, Day Case, and Outpatient waiting lists, focusing on the collection and validation of patient data. For Outpatient (OP) Waiting Lists, the report highlights the total number of patients awaiting their first appointment at a consultant-led clinic, with specific confidentiality measures for small volume counts. Adult/Child classification is based on hospital designations, and the data, captured monthly, is the responsibility of individual public hospitals, ensuring accuracy and integrity. Notes for consideration include details on specific hospitals' data inclusion/exclusion, system upgrades affecting data submission, and standardization of time band categories. The Inpatient and Day Case (IPDC) Waiting List report follows a similar structure, emphasizing confidentiality, data classification, and responsibility for accurate reporting, with additional notes on standardized time band categories and updates for specific hospitals impacted by system upgrades.
### **Problem Statement:**
The current issue revolves around inefficiencies in maintaining and extracting insights from patient waiting list data at Group Hospital. Currently, there is a lack of a comprehensive and user-friendly system for monitoring real-time waiting list statuses, and available specialties, as well as the capacity for analyzing historical patterns in inpatient and outpatient categories and doing thorough specialty-level and age profile assessments. Stakeholders suffer from an absence of a centralized and visually intuitive solution, which limits their capacity to make informed choices promptly. 
### **The 9-BA/BI Steps For Dashboard Development**
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
#### **1. Requirement Gathering**
This is the most important step of dashboard creation. The effectiveness of your dashboard/report is determined by its 
capacity to address the specific business need/problem, not by its visual attractiveness. 
Under requirement gathering, there are 4 sequential steps for gathering the requirements for your dashboard/reports, so you can offer value to your stakeholders.

- **Identify Stakeholders:**
    Determine the primary stakeholders and establish a point of contact, such as domain experts or leaders who will utilize the dashboard. Setting a point of contact at the outset is crucial for seeking explanations and clarifications as needed. For this particular project, we identify the stakeholders as Hospital Administrators, Department Heads, Medical Staff, Data Analysts/IT Department, Quality Assurance Team, Patients, Government Health Agencies, and Hospital Board Members

- **Understand Business Objectives:**
    the next step is to engage in meetings and calls with stakeholders to obtain a comprehensive outline of goals for the entire endeavor. his will include setting up meetings via skype, google meet, team meeting etc depending on the type of organization and the tools they use for collaboration. You have to ask open-ended questions during these discussions aids in gaining deeper insights into the data and understanding how the dashboard aligns with specific business goals. From the problem statement, we identify 3 key objectives:

    * Track the current status of patients' waiting lists.
    * Analyze historical monthly trends for inpatient and      outpatient categories.
    * Perform detailed specialty-level and age profile analyses.

- **Understand Business Objectives:**
    Having identified your stakeholders, the next step is to engage in meetings and calls with stakeholders to obtain a
    comprehensive outline of goals for the entire endeavor. This will include setting up meetings via skype, google meet, team
    meeting etc depending on the type of organization and the tools they use for collaboration. You have to ask open-ended 
    questions during these discussions aids in gaining deeper insights into the data and understanding how the dashboard 
    aligns with specific business goals. From the problem statement, we identify **3 key objectives:**

    * Track the current status of patients' waiting lists.
    * Analyze historical monthly trends for inpatient and outpatient categories.
    * Perform detailed specialty-level and age profile analyses.

- **High-Level Data Study:**
    Conduct a high-level overview of the data, focusing on key aspects without delving into detailed analysis. Topics to cover include data source, column descriptions, data types, volume, frequency, and data quality (identifying missing values or anomalies).

- **Define Scope:**
    Engage in discussions with stakeholders to define the scope, discussing key metrics, KPIs, and deployment timelines.
    Document calculations, timeframes, and scope details during this stage to set clear expectations and avoid future disagreements.

###### TIP: Follow 80-20 Rule:
When estimating your ETA, as a best practice, adhere to the 80-20 rule, keeping a 20% buffer while finalizing deadlines.
This ensures a margin for over-delivering beyond standard commitments and mitigates the risk of falling short after an initially extraordinary pitch.


#### **2. Data Collection**
Data collection is a crucial step in creating a Power BI dashboard for meaningful analysis. During this phase, information is gathered from diverse sources and brought into the Power BI platform. With over 200 data connectors available, choosing the right one is key. In this example, the focus is on using the folder connector, where a central folder holds all the needed files for refreshing the dashboard. The chosen data source involves separate files for inpatient and outpatient data in yearly folders. Ensuring uniformity in columns and headers across files is vital. The process includes clicking "Get Data," selecting the folder connector, specifying the folder path, and previewing the data. Users can then choose to combine and load the data for deeper analysis.
#### **3. Data Transformation and Modeling**
Now that the inpatient and outpatient data is loaded into Power BI, the next step is to apply transformations. By clicking on the small icon and selecting "Transform Data," the Power Query Editor is opened. In this editor, the tables loaded into Power BI are displayed on the left, and the user can review and manipulate the data. Checking data types and ensuring consistency is crucial, and any transformation steps are recorded in the applied step section on the right, allowing for easy tracking and correction of mistakes. The demonstration emphasizes checking and adjusting data types, reviewing columns, and verifying row counts for both inpatient and outpatient data.
#### **4. Data Visualization Blueprint**
The team is now focusing on creating a data visualization blueprint for the dashboard. After gaining a detailed understanding of the data through transformations and modeling, the team collaborates in a brainstorming session to finalize the dashboard's structure. Two main pages are planned: 
- **a summary page** and a 
- **detailed granular level page**. 
The summary page will feature visuals like the total waiting list for the current month, a comparison with the previous year, and various average waiting list trends. Special attention will be given to specialties, including both average and median metrics to address outliers. Essential filters for month, case type, and specialty will be incorporated. The detailed page is designed for in-depth data exploration, focusing on advanced visualization features for an improved user experience. This blueprint guides the direction for dashboard development, setting the stage for the next phase of actually designing the dashboard.
#### **5. Dashboard Layout and Design**
In the design phase, the focus shifts to building the charts outlined in the data visualization blueprint. Before starting the design process, it's recommended to enable two options in the view tab: grid lines and snap to grid, aiding in better alignment of objects. **_The top-left section requires two numbers_**, showcasing the current month wait list versus the same month of the previous year. Utilizing DAX, a measure named "latest month wait list" is created to dynamically display the current month's wait list. See DAX code below:

![current and previous year to date](https://github.com/drsNdamah/About-Me/assets/111310572/6fc2507a-5af6-4e2b-a25c-4d5e370ffb19)


```
Latest Month Wait List = CALCULATE(SUM(All_Data[Total]), All_Data[Archive_Date] = MAX(All_Data[Archive_Date]))

```

Similarly, another measure, "py latest month wait list," is crafted to represent the previous year's same-month wait list.

```
PY Latest Month Wait List = CALCULATE(SUM(All_Data[Total]), All_Data[Archive_Date] = EDATE(MAX(All_Data[Archive_Date]), -12))+0
```

Moving to the middle section, three different charts are planned: a donut chart for case types, a stacked column chart for age profile and time band relationship, and a matrix displaying top 5 specialties with average and median wait list metrics. To toggle between average and median metrics, a mechanism is introduced using a slicer. DAX measures "average wait list" and "median wait list" are created to dynamically switch between these metrics.

![middle](https://github.com/drsNdamah/About-Me/assets/111310572/d838f01b-c2bc-4daf-b463-dbc689cb0e8a)

For Average/Median, I used the following DAX code:
- Average

```
Average Waiting List = AVERAGE(All_Data[Total])
```

- Median
```
Median Waiting List = MEDIAN(All_Data[Total])
```
- Switch Statement to toggle between the two metrics
```
Avg/Med Wait List = SWITCH(VALUES('Calculation Method'[Calc Method]), "Average", [Average Waiting List], "Median", [Median Waiting List])
```
Of course, the switch statement above indicates that I need to create table called 'Calculation Method' to facilitate the switch:

- Calculation Method Table

![Calc Table](https://github.com/drsNdamah/About-Me/assets/111310572/9a24bfc0-773a-4e1d-a5f5-7c6efc2b0931)


The bottom section includes two line charts for inpatient and outpatient cases. The design also incorporates filters for month, case type, and specialty, enhancing the dashboard's overall functionality. The second page, named "detail," is created for more granular exploration. The design elements from the summary page are copied, including filters, ensuring synchronization between the two pages. The detailed view is designed using a matrix for better data exploration.

![trendz](https://github.com/drsNdamah/About-Me/assets/111310572/89245981-e1ca-42bb-badd-7ac12af89dac)


- Detailed Page

![image](https://github.com/drsNdamah/Healthcare-EIS-PowerBi/assets/111310572/24b0512d-4519-426e-b008-9c156df7e8e6)

#### **6/7. Adding Interactivity / Navigation and Testing**
In this phase of the project, the focus is on enhancing the dashboard's interactivity, navigation, and addressing potential issues. To begin, filters are refined to handle scenarios where data might be missing, providing a more seamless user experience. For instance, when changing date filters, steps are taken to display zero instead of a blank, ensuring a cleaner appearance. 
I added + 0 to the calculation so that if the 'Archive_Date' filter is set to a date value outside of the range, it will simple return 0.

```
Latest Month Wait List = CALCULATE(SUM(All_Data[Total]), All_Data[Archive_Date] = MAX(All_Data[Archive_Date]))+0
```

```
PY Latest Month Wait List = CALCULATE(SUM(All_Data[Total]), All_Data[Archive_Date] = EDATE(MAX(All_Data[Archive_Date]), -12))+0
```

To manage interactions between filters and charts, I use 'manage relationship' under the Modeling tab to ensure that I selectively enable or disable interactions. This ensures that specific charts remain unaffected by certain filter changes, optimizing the user's understanding of the data.

- Controlliing How Visuals Display When There is no Data
Addressing the visibility issue when selecting certain specialties, a dynamic "no data" text is introduced to indicate the absence of data for a particular selection. This involves creating new measures and using DAX formulas to display relevant messages. At the moment, when you select certain with values in the specialty name slicer, some of the visuals show blank or empty. This has been fixed with the DAX below:

![image](https://github.com/drsNdamah/About-Me/assets/111310572/a7f8723b-884d-4f41-8830-07716ea47052)


- for the left visual
```
NoDataLeft = if(ISBLANK(CALCULATE(SUM(All_Data[Total]), All_Data[Case_Type]<> "Outpatient")), "No data for selected criteria", "")
```
- for the right visual

```
NoDataRight = if(ISBLANK(CALCULATE(SUM(All_Data[Total]), All_Data[Case_Type] = "Outpatient")), "No data for selected criteria", "")
```

- After this the visual looks like this:
![image](https://github.com/drsNdamah/About-Me/assets/111310572/994182a4-4b81-4cbf-b1ba-3c6b39a6bb74)

