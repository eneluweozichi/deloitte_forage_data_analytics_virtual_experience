### Daikibo Manufacturing: Machine Downtime Analysis Using Tableau

**Project Overview**

This project was completed as part of the Deloitte Data Analytics Virtual Job Simulation on Forage.

The project involved analysing machine telemetry data collected from Daikibo, a manufacturing company operating four factories across Japan, Germany and China.

The objective was to investigate machine downtime across the manufacturing facilities, identify the factory experiencing the highest downtime and determine which machine type contributed most to downtime within that facility.

Tableau was used to transform the raw telemetry data into interactive visualizations to support operational decision-making.

**Business Problem**

Daikibo collected machine telemetry data from its four manufacturing facilities over May 2021. The company wanted to gain insights into equipment performance and identify potential operational inefficiencies.

The analysis was designed to answer two key business questions:

1. Which factory experienced the highest machine downtime?
2. Which machine type experienced the highest downtime within that factory?

**Dataset Overview**

The dataset was provided as a compressed JSON file and contained approximately 10,000 records across 11 columns.

Key variables included:

Area

City

Country

Device ID

Device Type

Document Index

Factory

Section

Status

Temperature

Timestamp

**Data source**: Deloitte Forage – Daikibo Telemetry Dataset.

**Data format**: JSON (ZIP archive).

**Tools and Technologies**

Tableau – Data visualization and interactive dashboard development.

Calculated Fields – Data transformation and downtime measurement.

**Data Preparation and Transformation**

The original JSON file was extracted from its ZIP archive and imported into Tableau.

A calculated field named Unhealthy was created to convert machine operational status into a numerical downtime measure.

Tableau calculated field:

IF [Status] = "Unhealthy"
THEN 10
ELSE 0
END

Each unhealthy telemetry status was assigned a value of 10, representing 10 minutes of potential downtime, while healthy statuses were assigned zero.

This transformation made it possible to aggregate potential downtime across factories and machine types.

**Data Visualization and Dashboard Development**

Two bar charts were developed:

1. **Downtime Per Factory**
This visualization compared accumulated machine downtime across the four manufacturing facilities.

2. **Downtime Per Machine Type**
This visualization compared accumulated downtime across the nine machine types.

The factory chart was configured as a dashboard filter. Selecting a factory dynamically updated the machine-type chart to display the downtime distribution for that specific facility.

This interactivity enabled a more focused investigation of machine performance.

## Dashboard Preview

### Overall Downtime Analysis
![Overall Downtime Dashboard] (https://github.com/eneluweozichi/deloitte_forage_data_analytics_virtual_experience/blob/main/Dashboard/Daikibo_Downtime_Dashboard.png?raw=true)

### Seiko Factory Filtered Analysis
![Seiko Factory Filtered Dashboard](./Dashboard/Seiko_Filtered_Downtime.png)

**Key Findings**

The analysis identified Daikibo Factory Seiko in Osaka, Japan, as the facility with the highest accumulated downtime.

After selecting this factory using the dashboard filter, the machine-type visualization identified LaserWelder as the machine type with the highest accumulated downtime.

**Key result:**

Factory: Daikibo Factory Seiko

Location: Osaka, Japan

Highest downtime machine type: LaserWelder

Accumulated downtime: 480 minutes (8 hours)

**Business Recommendation**

Daikibo should prioritize investigating the LaserWelder machines at its Seiko facility.

Further equipment inspections and maintenance assessments could help identify the causes of repeated unhealthy machine statuses and reduce potential production interruptions.

The findings can also support preventive maintenance planning and more effective allocation of maintenance resources.

**Skills Demonstrated**

Data exploration

JSON data importation

Tableau calculated fields

Data transformation

Data visualization

Interactive dashboard development

Business problem-solving

Analytical interpretation and reporting

**Project Deliverable**

An interactive Tableau dashboard comparing factory downtime and machine-type downtime.

The dashboard enabled factory-level filtering to identify the machine type contributing most to downtime within the highest-downtime facility.
