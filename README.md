# HR-analytics-Dashboard-


# 🧾 HR Analytics Dashboard – Workforce Trends & Attrition Insights

## 📊 Overview
This Power BI dashboard provides a comprehensive analysis of workforce trends and employee attrition.  
The goal of this project is to help the HR department understand factors affecting employee engagement, satisfaction, and turnover, and support data-driven retention strategies.

---

## 🧠 Key Objectives
- Analyze workforce composition and attrition patterns.  
- Identify high-risk departments and age groups with higher turnover.  
- Understand how factors like salary, training, and work-life balance impact job satisfaction.  
- Enable HR to take informed, data-driven decisions to reduce attrition and improve employee engagement.

---

## 📁 Dataset Description
The dataset contains employee-level information such as:
| Category | Example Columns |
|-----------|----------------|
| **Demographics** | Age, Gender, Marital Status, Education Field |
| **Work Details** | Department, Job Role, Business Travel, Job Level |
| **Performance & Engagement** | Job Satisfaction, Work Life Balance, Environment Satisfaction |
| **Financials** | Monthly Income, Daily Rate, Stock Option Level |
| **Tenure & History** | Years at Company, Years with Manager, Years Since Last Promotion |
| **Attrition** | Yes/No – Indicates whether the employee has left the organization |

This data is suitable for HR analytics since it combines demographic, engagement, and financial indicators.

---

## ⚙️ DAX Measures Used

```DAX
-- Total Employees
Total Employees = COUNTROWS('HR_Data')

-- Attrition Count
Attrition Count =
CALCULATE(
    COUNTROWS('HR_Data'),
    'HR_Data'[Attrition] = "Yes"
)

-- Attrition Rate
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees]
) * 100

-- Average Monthly Income
Average Income = AVERAGE('HR_Data'[Monthly_Income])

-- Average Years Worked
Average Years = AVERAGE('HR_Data'[Years_At_Company])





📈 Visuals Included
Visual	Purpose
KPI Cards	Show high-level metrics like total employees, attrition rate, average income, etc.
Bar Chart (Attrition by Department)	Identifies which departments have the highest attrition.
Bar Chart (Attrition by Age Band)	Highlights which age groups are leaving more often.
Donut Chart (Attrition by Gender)	Displays gender composition and attrition ratio.
Line Chart (Monthly Income vs Years at Company)	Shows how salary increases with experience.
Line Chart (Training Times vs Job Satisfaction)	Visualizes the relationship between training frequency and satisfaction.
Column Chart (Work Life Balance vs Job Satisfaction)	Shows how better balance leads to higher satisfaction.
Bar Chart (Average Salary by Job Role)	Compares pay levels across different job roles.
Demographics Chart (Department vs Attrition)	Shows employee count and attrition distribution.
🧩 Insights & Findings

R&D and Sales departments show the highest attrition.

Employees aged 25–44 are most likely to leave.

Work-life balance and training strongly influence job satisfaction.

Average salary increases with tenure, indicating fair career progression.

Male attrition slightly exceeds female attrition, suggesting possible workload imbalance.

🧮 Technical Details

Tool Used: Microsoft Power BI

Language: DAX (Data Analysis Expressions)

Model Type: Single-table model (flat dataset)

Joins: Not required — dataset already consolidated

Filters/Slicers: Department, Gender, Education Field

🎯 Conclusion

This HR Analytics Dashboard successfully highlights critical workforce patterns and engagement factors.
It allows HR managers to monitor turnover rates, track satisfaction levels, and make better retention decisions.
The insights suggest focusing on work-life balance, training opportunities, and retention strategies for high-attrition departments.

👤 Author

Name: Somya Vats
Institute: School of Computer Science, UPES Dehradun
Project: Power BI HR Analytics Dashboard
Dataset Source: Company HR Dataset
Visualization: Power BI by Somya Vats
