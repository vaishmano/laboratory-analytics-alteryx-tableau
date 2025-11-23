# laboratory-analytics-alteryx-tableau
End-to-end diagnostic laboratory analytics project using Alteryx for data engineering and Tableau for dashboard visualization. Includes data cleaning, feature engineering, predictive rolling averages, and an interactive performance dashboard.

📘 Laboratory Insights & Performance Dashboard
Built Using Alteryx + Tableau
📌 Project Overview

This project demonstrates an end-to-end data analytics workflow using Alteryx for data preparation and Tableau for dashboard visualization.
The dataset simulates diagnostic laboratory operations similar to real workflows in companies like Vibrant America.

The project includes:

Data cleaning, joining, and enrichment

Feature engineering for predictive insights

Multi-row rolling average calculations

Outlier detection

Geographic and operational analysis

An interactive Tableau dashboard

This showcases strong capability in ETL, analytics, BI visualization, and data storytelling.

🧰 Technologies Used
Category	Tools
Data Engineering	Alteryx Designer
Visualization	Tableau Desktop
Documentation	Word / PDF
Version Control	GitHub
📂 Project Structure
├── data/
│   ├── vibrant_tests.csv
│   ├── vibrant_patients.csv
│   └── vibrant_output.xlsx
│
├── alteryx-workflow/
│   └── lab_processing_workflow.yxmd
│
├── tableau/
│   └── lab_insights_dashboard.twbx
│
├── documentation/
│   ├── Alteryx_Workflow_Documentation.docx
│   └── Dashboard_Description.pdf
│
└── README.md

🛠️ Alteryx Data Engineering Workflow

The data was prepared using Alteryx Designer, performing transformation, enrichment, and predictive feature creation.

1. Input Data

vibrant_tests.csv → test results

vibrant_patients.csv → patient demographics

2. Cleaning & Formatting

Converted ResultDate into proper Date type

Removed null or invalid PatientIDs

Standardized numeric fields

3. Joining

Merged both datasets using PatientID.

4. Feature Engineering

Created analytical fields:

Field	Purpose
PriorResultAvg	Mean of earlier results per patient
DeltaFromPrior	Change from previous result
IsOutlier	Flags abnormal result deviations
RollingAvg3	Predictive smoothing (3-point rolling average)
AgeGroup	Categorized age buckets
ProcessingBucket	Time-to-process grouped into 0–60, 60–120, 120+ mins
5. Output

Exported final cleaned dataset to Excel for Tableau.

📊 Tableau Visualizations
1️⃣ Test Result Trend Over Time

A line chart showing how average test results change each year, revealing long-term patterns, spikes, and patient severity trends.

2️⃣ Patient Distribution Across U.S. States

A filled map showing where laboratory tests originate.
Darker states represent higher patient/test volume.

3️⃣ Number of Tests by Panel Type

Compares test counts across Autoimmune, Cardiac, Hormone, Influenza, and Metabolic panels.
Shows workload distribution and test popularity.

4️⃣ Rolling 3-Point Average vs Actual Results

Dual-axis line visualization comparing real test values vs a predictive rolling average.
This highlights volatility, stability, and underlying patterns.

5️⃣ Turnaround Time Performance

Bar chart showing how many tests fall into each processing-time category:

0–60 mins

60–120 mins

120+ mins

Helps identify operational efficiency and bottlenecks.

📊 Dashboard Overview
Dashboard Name:

Laboratory Insights & Performance Dashboard

Purpose:

To provide a comprehensive view of diagnostic trends, patient distribution, test workloads, predictive behavior, and operational performance.

Dashboard Includes:

Yearly trend in test results

Geographic distribution of patients

Test volume by panel type

Rolling average vs actual results

Turnaround time performance

⭐ Key Insights

Certain years show higher average test results → possible rise in abnormal cases

Highest patient volumes in CA, TX, WA, PA

Metabolic & Cardiac panels are most frequently ordered

Rolling averages reveal stable underlying trends

Majority of tests fall into the 120+ mins bucket → operational improvement opportunity

🚀 How to Use
Run Alteryx Workflow

Open .yxmd in Alteryx

Run workflow

Export the output Excel file

Open Tableau Dashboard

Open .twbx file

Refresh data source to the exported Excel

Explore filters: State, Test Panel, Result Flag, Age Group

👩‍💻 Author

Vaishnavi Manogaran
Master’s Student – International Information Systems (FAU)
Portfolio project demonstrating skills in Alteryx, Tableau, ETL pipelines, and analytics.
