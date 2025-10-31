# **EMPLOYEES ATTRITION ANALYSIS**

## **Background**
Lately, I've been hearing a lot of information about how the younger generation is quitting their jobs and quickly hopping to new ones. When a company chooses not to refill those roles, it leads to employee attrition. This can be a strategic cost-saving measure but also risks overloading remaining staff and creating critical skill gaps. In this project, I will use IBM employee data to analyze the primary reasons why people leave in these situations. The end goal is to deliver clear, data-driven suggestions to help businesses manage attrition strategically, protect team morale, and retain their most valuable talent.

## **Questions to be Analyzed**
1. What is the overall extent of employee attrition look like?
2. What kinds of jobs and departments have a high attrition rate?
3. What is the biggest factor that influences employee attrition?
4. How does compensation disparity influence attrition across an employee's career lifecycle?

## **Tools**
I will use Microsoft Excel to analyze this dataset and present the insights efficiently. Specifially, I am going to utilize these features in order to help me analyze and present better insights:
- Power Query
- PivotTable & PivotCharts
- Power Pivot

## **Dataset Information**
The dataset used for this project contains a fictional dataset created by [IBM](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) data scientist that contains detailed information of employees in a company. I will also provide about the dataset's license that you can click [here](https://opendatacommons.org/licenses/dbcl/1-0/)

## **Steps to Analyze**
### Data Preparation
1. **Data Import & Initial Review**: I began by importing the raw dataset into Excel using Power Query. My first step was to thoroughly scan each column using filters to check for data quality issues, including missing values, incorrect data types, and inconsistencies.
2. **Data Transformation Planning**: During the review, I identified several columns containing numeric codes that represented categorical scores (e.g., 1 = "Low" for Job Satisfaction). To make the data more intuitive for analysis, I planned to convert these numbers into their descriptive text labels according the [IBM](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) dataset.
3. **Creating a Cleaned Dataset**: I added an index to the raw dataset for traceability and created a new Power Query named Values_Cleaned. This query was designed to hold the index and all the columns requiring value transformation.
4. **Value Standardization**: Within the Values_Cleaned query, I created new columns to transform the numeric codes into their corresponding descriptive text. After this step, the original numeric columns were removed to avoid redundancy.
5. **Final Data Merge & Structuring**: I merged the original dataset with the new Values_Cleaned query using the index as a key. Finally, I removed obsolete columns, renamed others for clarity, and reordered the entire dataset to create a clean, well-structured table ready for analysis.
6. **Quality Assurance Check**: Finally, I performed a quick skimming of the merged dataset to ensure all transformations were successful, data integrity was maintained, and the dataset was ready for analysis.

<img width="857" height="361" alt="Cleaning Data" src="https://github.com/user-attachments/assets/bbad0eb3-4950-492b-a77a-858d6a9f5df1" />


### Data Analysis
To answer the business questions, I performed a systematic exploration of the dataset in this sequences:
1. **Establishing the Baseline**: I first calculated the company's overall attrition rate to understand the scale of the problem.
2. **Identifying Problem Areas**: I segmented the attrition rate by department and job role to locate where the issue was most concentrated.
3. **Analyzing Driving Factors**: I conducted a focused analysis on two fronts:
   - External Factors: I measured the impact of tangible job conditions like overtime, compensation, and business travel on attrition rates.
   - Internal Factors: I evaluated the influence of psychological elements, including job satisfaction, work-life balance, and relationships at work.
4. **Investigating Career Progression**: I explored the relationship between employee tenure, compensation, and their decision to leave the company.

This structured approach allowed me to move from a general understanding of the problem to specific, actionable insights.

## **Insights**
1. **Q1: What is the overall extent of employee attrition?**
The company has a significant attrition problem, with a rate of 16.1%. This means that over the period analyzed, 237 employees left the organization and were not replaced. This level of turnover represents a substantial cost in recruitment, knowledge lost, and operational disruption, establishing a clear need for a strategic intervention.

<img width="2082" height="1172" alt="Q1-Overall Attrition" src="https://github.com/user-attachments/assets/1144f225-4a06-48ec-8c88-4b3ca7f8a3e8" />

2. **Q2: What kinds of jobs and departments have a high attrition rate?**
The problem is not evenly distributed. The Sales department is the most critical hotspot with an alarming 20.6% attrition rate. Drilling down, the Sales Representative role is in crisis, with 4 out of every 10 employees (39.8%) leaving. From a volume perspective, the larger Research & Development department contributes the most to the problem (56% of all leavers), with Laboratory Technicians being the single largest group of leavers. This indicates a targeted issue in Sales and a widespread, high-impact issue in R&D.

<img width="2082" height="1172" alt="Q2A-DeptAttr" src="https://github.com/user-attachments/assets/d24fca48-22c1-4832-912a-c8bb95f501ae" />

<img width="2082" height="1173" alt="Q2A-JobAttr" src="https://github.com/user-attachments/assets/8f1a0797-fc85-4e95-9fbb-ec49a3b28aa3" />

<img width="2082" height="1172" alt="Q2B-DeptLeavers" src="https://github.com/user-attachments/assets/2d73ae31-44db-4d3d-b1d4-4db05938d691" />

<img width="2082" height="1172" alt="Q2B-JobLeavers" src="https://github.com/user-attachments/assets/f6103de5-b65b-412e-a5b8-61b88feebc60" />

3. **Q3: What is the biggest factor that influences employee attrition?**
The analysis examined both external, tangible factors and internal, psychological factors. While internal factors like low satisfaction show a clear correlation, the most powerful drivers are external. A culture of overwork is the dominant issue, with employees who work Overtime leaving at a 30.5% rate and those reporting a "Bad" work-life balance leaving at 31.2%. This combination, alongside the 29.3% attrition rate for Below Average earners, shows that tangible job conditions and compensation are the most critical levers for reducing turnover.

<img width="2082" height="1173" alt="Q3-ExtFactors" src="https://github.com/user-attachments/assets/7cac8db8-3124-4bbb-99a7-9cce1cc613d8" />

<img width="2082" height="1172" alt="Q3-IntFactors" src="https://github.com/user-attachments/assets/16d2dcba-f11c-4ebf-9686-c9a880f958d6" />

4. **Q4: How does compensation disparity influence attrition across an employee's career lifecycle?**
Compensation's role in attrition changes dramatically over an employee's tenure. A massive pay gap of nearly $1,850 exists for early-tenure employees (0-2 years), making low starting salaries a primary reason new talent leaves. However, this trend reverses for long-serving employees (11+ years), where those who leave were actually paid more. This suggests the company successfully retains early-career employees with competitive growth but fails to hold onto its most experienced and likely high-performing veterans.

<img width="2082" height="1173" alt="Q4-Income" src="https://github.com/user-attachments/assets/a9bab9a5-e1cb-4201-9c4c-357e95b452eb" />

## **Conclusions**
This analysis reveals that employee attrition is not a single problem but a symptom of several interconnected issues. Culture of overwork is the primary driver, pushing out talent through burnout and poor work-life balance. A significant early-career pay gap makes new talent feel undervalued, a problem that is most severe in the critical frontline roles of Sales and R&D. To build a more stable and engaged workforce, the company must shift its focus from mere retention to fundamentally improving the daily employee experience.

## **Limitation**
While this analysis provides clear insights into attrition drivers, it's important to acknowledge some of its limitations:
1. **Data Quality**: The PerformanceRating column was unusable for analysis, as all employees were rated "Excellent" or "Outstanding." This suggests either severe rating inflation or a data integrity issue, preventing any meaningful analysis of how performance influences attrition.
2. **Correlation vs. Causation**: This analysis identifies factors associated with attrition, but it cannot definitively prove they are the cause. Unmeasured variables (e.g., management style, team dynamics) likely also play a role.
3. **Self-Reported Satisfaction**: Satisfaction scores are subjective and can be influenced by an employee's immediate mood or circumstances, which may not fully reflect their long-term experience.

