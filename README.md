# 📊 Employee Overview Dashboard

An interactive **Human Resource Analytics Dashboard** built in **Power BI** to help visualize and explore employee data including demographics, performance, engagement, and attrition.

---

## 📁 Dataset

The dashboard uses the **HRDataset_v14**, containing employee records with attributes such as:

- Demographics (Age, Gender, Race, Marital Status, Citizenship)
- Employment details (Department, Position, Manager, Hire Date, Termination Date)
- Performance metrics (Performance Score, Engagement, Satisfaction)
- HR data (Salary, Absences, Special Projects, Days Late)

---

## 🧩 Features

- 📌 **Dynamic slicers** for Department, Position, Employment Status, Gender, Date of Hire, and more
- 📈 KPIs: Total Employees, Attrition Rate, Avg Tenure, Engagement Score
- 📊 Charts for:
  - Employees by Department
  - Gender and Race Distribution
  - Salary Histogram
  - Performance & Satisfaction Analysis
  - Termination Trends
- 🔍 Drill-down capabilities and cross-filtering interactions
- 🎨 Clean layout with slicers and filters for deep insights

---

## 📷 Screenshots

| Overview Page | Demographics Page |
|---------------|-------------------|
| ![image](https://github.com/user-attachments/assets/1d767c6f-5ffb-4adc-86ce-ff8e07f7287e)| ![image](https://github.com/user-attachments/assets/64add0a9-252b-4529-a14d-a99cf68501d8)|

---

## 🛠️ Tools Used

- **Power BI Desktop**
- DAX (Data Analysis Expressions)
- Power BI Slicers & Filters
- Calculated Columns and Measures

---

## 🧠 Key DAX Measures

```dax
Attrition Rate = 
DIVIDE(
    CALCULATE(COUNT(HRDataset_v14[EmpID]), HRDataset_v14[Termd] = 1),
    COUNT(HRDataset_v14[EmpID])
)

Average Tenure = AVERAGE(HRDataset_v14[Tenure (Years)])

Active Employees = 
CALCULATE(COUNT(HRDataset_v14[EmpID]), HRDataset_v14[Termd] = 0)
```
