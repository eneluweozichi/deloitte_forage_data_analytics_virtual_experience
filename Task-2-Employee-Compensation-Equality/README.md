## Employee Compensation Equality Analysis

**Project Overview**

This project was completed as part of the Deloitte Data Analytics Virtual Job Simulation on Forage.

The task involved investigating employee compensation equality across different Daikibo manufacturing locations and job roles.

Following internal complaints concerning gender inequality in salary distribution, the Forensic Technology team developed an algorithm to quantify the level of gender pay equality across job roles and company locations.

My responsibility was to organize the supplied equality data, classify the equality scores, and prepare the dataset for further analysis using Microsoft Excel.

**Business Problem**

Daikibo Industries wanted to investigate potential gender-related salary inequalities across its manufacturing facilities.

The objective was to classify the equality scores into meaningful categories to help identify job roles and locations that may require further investigation.

**Dataset Overview**

The raw dataset was provided in an Excel format and contained approximately 37 rows with 3 columns. 1 extra calculated column was added resulting to 4 coolumns.

The dataset contained the following fields:

| Column | Description |
|---|---|
| Factory | Manufacturing location where the job role is situated |
| Job Role | Employee job position within the organisation |
| Equality Score | Numerical score representing the level of gender pay equality |
| Equality Class | Classification assigned based on the equality score |


**Tools and Technologies**
- Microsoft Excel
- Excel formulas
- Data entry and organization
- Data classification
- Data Preparation and Analysis

The initial dataset contained factory names, job roles and their corresponding equality scores.

I organized the information into a structured Excel table and created an additional column named Equality Class.

Using a nested IF formula combined with OR and AND logical functions, I classified the equality scores into three categories:

| Equality Score | Classification |
|---|---|
| -10 to +10 | Fair |
| Below -10 to -20, or above +10 to +20 | Unfair |
| Below -20 or above +20 | Highly Discriminative |

**Excel Formula**
=IF(OR(C2<-20,C2>20),"Highly Discriminative",IF(AND(C2>=-10,C2<=10),"Fair","Unfair"))

The formula automatically evaluated each equality score and assigned the appropriate classification.

### Key Findings

1. **Overall Analysis**

A total of 37 records were analysed across four Daikibo manufacturing facilities.

The equality scores were classified into three categories:
| Equality Classification | Number of Records | Percentage |
|---|---:|---:|
| Fair | 19 | 51% |
| Unfair | 11 | 30% |
| Highly Discriminative | 7 | 19% |
| **Total** | **37** | **100%** |

**Observation**

Although 51% of the records were classified as Fair, the remaining 49% fell into the Unfair and Highly Discriminative categories. This indicates potential compensation equality concerns that warrant further investigation.

2. **Factory-Level Analysis**

| Factory | Unfair | Highly Discriminative | Total Concerning | Total Records | Concerning % |
|---|---:|---:|---:|---:|---:|
| Daikibo Factory Meiyo | 4 | 3 | 7 | 11 | 64% |
| Daikibo Factory Seiko | 2 | 3 | 5 | 10 | 50% |
| Daikibo Berlin | 3 | 0 | 3 | 8 | 38% |
| Daikibo Shenzhen | 2 | 1 | 3 | 8 | 38% |

#### Major Findings

**Daikibo Factory Meiyo**

Meiyo recorded the highest concentration of concerning equality scores, with 7 out of 11 records (64%) classified as Unfair or Highly Discriminative.

**Daikibo Factory Seiko**

Seiko recorded 5 concerning records out of 10 (50%), including 3 Highly Discriminative records.

**Daikibo Berlin**

Berlin recorded 3 concerning records out of 8 (38%). All three were classified as Unfair.

**Daikibo Shenzhen**

Shenzhen also recorded 3 concerning records out of 8 (38%), comprising 2 Unfair and 1 Highly Discriminative record.

3. **Key Business Insight**

Daikibo Factory Meiyo represents the highest-priority location for further compensation equality investigation based on the proportion of concerning equality scores.

Daikibo Factory Seiko also warrants attention because of its three Highly Discriminative records.

4. **Recommendations**
- Prioritize a detailed review of compensation practices at Daikibo Factory Meiyo.
- Investigate the job roles associated with Highly Discriminative scores at Meiyo and Seiko.
- Review the underlying salary and employee data to understand the factors contributing to the observed equality scores.
- Conduct periodic compensation equality assessments across all manufacturing facilities.
- Ensure that compensation decisions are supported by consistent and transparent criteria.

6. **Analytical Limitation**

The analysis is based on 37 supplied records and the equality scores provided. The results identify potential areas of concern but do not establish the causes of the differences or prove discriminatory treatment.

**Skills Demonstrated**
- Data entry and data organization
- Data cleaning and structuring
- Excel formulas and logical functions
- Conditional classification
- Attention to detail
- Analytical thinking
- Data interpretation

**Project Deliverable**

A structured Excel dataset containing factory locations, job roles, equality scores and their corresponding equality classifications.

**Conclusion**

This exercise demonstrated how spreadsheet tools and logical functions can be applied to organize and classify business data.

The resulting dataset provides a foundation for identifying potential compensation equality concerns across different manufacturing locations and job roles.




