# Salifort Motors Attrition Analysis
Analyzing 10k+ employee profiles to identify the leading attrition cause and create a retention strategy.

## 📖 Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Data Source](#data-source)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Key Findings & Insights](#key-findings--insights)
- [Model Construction](#model-construction)
- [Next Steps](#next-steps)
- [Conclusion](#conclusion)
- [Contact](#contact)

---

## 📌 Overview
This project analyzes cross-sectional data of employee profiles to answer what drives attrition in Salifort Motors. The goal is to transform raw data into actionable insights that can help the HR department and executives make data-driven decisions for policy revision to increase retention.

## 🎯 Problem Statement
The core challenge addressed in this analysis is:
Employee turnover rate is recorded as high as 16.6% by the time the data is collected. We are tasked with constructing a machine learning model to predict turnovers. To construct the model, an analysis was conducted to identify the leading factors of attrition.

**Objectives:**
- Identify attrition trends within the dataset based on previous studies.
- Construct a machine learning model to predict turnovers.
- Provide recommendations to improve retention.

## 📂 Data Source
The dataset used for this analysis was obtained from Kaggle.
- **Record Count:** 1499 rows
- **Columns:** 10 features; ['satisfaction_level', 'last_evaluation', 'number_project',
       'average_montly_hours', 'time_spend_company', 'Work_accident', 'left',
       'promotion_last_5years', 'Department', 'salary']

*Note: The raw data has been cleaned and pre-processed. See the [Methodology](#methodology) section for details.*

## 🛠 Tools & Technologies
- **Data Extraction/Storage:** Python (Pandas)
- **Data Cleaning:** Python (Pandas, NumPy)
- **Exploratory Data Analysis (EDA):** Kaggle Notebook, Python (Matplotlib, Seaborn)

## 🔍 Methodology
This analysis followed a standard data analytics pipeline:

1. **Data Extraction & Loading:** Data was queried from Kaggle and loaded into Kaggle Notebook.
2. **Data Cleaning:**
   - Renamed columns into the appropriate snake case format
   - Handled duplicate values by dropping duplicate values.
3. **Exploratory Data Analysis (EDA):**
   - Cited previous attrition patterns from multiple sources
   - Compared trends in the dataset with patterns observed in previous studies
   - Performed bivariate analysis to test hypotheses regarding performance vs average_working_hours, performance vs project_count.
4. **Feature Engineering:** Created new metrics such as:
   - work_health (Employee's working condition based on their working hours)
   - tier (Employee's performance tier)

## 💡 Key Findings & Insights
Based on the analysis, the following insights were discovered:

- **Insight 1:** Normalized Overworking – Critical overworking is systematically favored; a dense population of high-performers is present in this threshold
- **Insight 2:** Over and Underutilization Patterns – Attrition spikes with overutilization and underutilization
- **Insight 3:** Low Internal Mobility – Excluding employees who left, there is a 1.95% 5-Year Promotion Incidence

## Model Construction
Based on the EDA findings, constructing a predictive attrition model is not recommended. Given that employees in Salifort Motors are working above the normal working hours and the legal overtime threshold on average, the ethical risks of constructing a prediction model are:

1. **Unfair incentives to retain employees:** The model might be used strictly to incentivize employees without rectifying humanitarian policies.
2. **Dehumanizing outcomes:** The model risks being used to manage individual employees through incentives rather than addressing systemic problems, treating retention as a technical problem instead of a management accountability issue.

On top of that, there are multiple dataset limitations worth considering.

- The abnormality of working hours within this dataset risks constructing a model that normalizes abnormal working hours.
- Given the cross-sectional nature of the dataset, models are only able to match attrition profiles between employees instead of calculating real risks.
- Given the lack of details on employee roles and project details, models cannot reliably predict without context.

## Next Steps
1. **Curbing Overtime:**
   - Revising Employee Evaluation Framework: HR should investigate why overworking is favored and make a data-driven solution to this issue.
   - Physical Overtime Guardrails: Executives can put forward a policy to curb overtime via physical means. Policies such as scheduled network downtimes, mandatory lights-off hours, or mandatory closing periods will make overtime unfavorable, thus normalizing standard hours
   - Systemic Overtime Guardrails: Employees with severe overworking should not be recompensated with monetary incentives, but with awarded leaves.
2. **Revising Workload Management:**
   - Increase Manager Accountability: Managers should be accountable for uneven workload management. Introducing managerial KPI standards that include Team Workload as a weightage will help track workload across teams.
   - Consider Outsourcing: Outsourcing will be a manageable step that can be taken to distribute the workload away from burnt-out employees.
3. **Increasing Internal Progression:**
   - Reskilling Low-Performing Employees: Reskilling helps keep healthy, low-performing employees engaged and feel seen, thus increasing retention.
   - Upskilling: A healthy upskilling policy within the company not only keeps the employees engaged, but it's also a valuable perk that increases retention.
   - Broadbanding: Introducing a wider salary range within the same position would increase internal progression without creating new seats or ladders for employees to climb
   - Lateral Mobility: HR should assess an employee's skill to find eligible adjacent roles outside of their posted department. Lateral mobility is a strategy to keep employees engaged

## Conclusion
This analysis implies that Salifort Motors is currently operating under a very unsustainable working culture that burns out its top talents, and at the same time underutilizes employees within normal working thresholds. On top of that, limited progression and internal mobility made it very hard for employees to find a reason to stay, as their efforts are unrecognized.



