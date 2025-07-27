# NDMC Talent Search Exam (NSTSE) Analysis Dashboard

This project showcases a real-world data analytics simulation of the **NDMC Schools' Talent Search Examination (NSTSE)** using Power BI. The dashboard presents insights into student performance, academic correlations, and scholarship distribution — **based on anonymized fictional data modeled after actual NDMC workflows.**

---

## 📊 Dashboard Overview

The dashboard provides an interactive overview of key performance indicators (KPIs) and visual analytics, including:

- 🔢 **Total Eligible Students**  
- 📈 **Average NSTSE Score**
- 🎯 **Scholarship Qualification Rate**
- 🧮 **Class-wise Scholarship Distribution**
- 📊 **NSTSE Score Histogram**
- 📉 **Academic vs NSTSE Score Scatter Analysis**
- 📋 **Student-wise Performance Table**

The visuals are interactive, with slicers for:
- Class
- Bank
- Scholarship Status
- NSTSE Score Range

---

## 📁 Dataset (Fictional)

The dataset was generated using ChatGPT and modeled to reflect NDMC’s actual examination structure, while maintaining full confidentiality of real student data.

### Tables Used:
- `Student_Personal_Info`: Basic info, address, and banking details
- `Student_Academic_Info`: Class and academic percentages
- `Student_Scholarship_Info`: NSTSE scores and scholarship status

These tables were connected using a **1-to-1 relationship on `student_id`**.

---

## 🔧 Tools & Techniques

| Tool | Purpose |
|------|---------|
| **Power BI** | Data visualization and DAX measures |
| **DAX** | For KPI calculations and dynamic measures |
| **SQL Server (notebook)** | Used earlier for data cleaning and shaping |
| **Excel** | Source of fictional data |

---

## 💡 Key DAX Measures

```dax
Total Students = COUNT(Student_Personal_Info[student_id])

Average NSTSE Score = AVERAGE(Student_Scholarship_Info[nstse_percent])

Qualified Students = 
CALCULATE(
    COUNT(Student_Scholarship_Info[student_id]),
    Student_Scholarship_Info[scholarship_alloted] = "Yes"
)

Qualification Rate (%) = 
DIVIDE(
    [Qualified Students],
    [Total Students],
    0
)

Average Academic Score = AVERAGE(Student_Academic_Info[previous_class_percentage])
```

---

## 📸 Sample Screenshots

> 📍 <img width="2767" height="1600" alt="NDMC Talent Search Exam (NSTSE) Analysis Dashboard-1" src="https://github.com/user-attachments/assets/57fc16b1-c57e-4707-8b14-92da81d8d2ab" />


---

## 🧠 Insights Uncovered

- Despite high academic scores, a relatively low scholarship qualification rate suggests the NSTSE is competitive.
- Some students with mid-range academic performance scored very well in NSTSE.
- Certain classes (like XI & XII) had higher participation but not necessarily higher qualification rates.

---

## 📎 Files Included

| File | Description |
|------|-------------|
| `Delhi_Students_Data.xlsx` | Fictional dataset (3 related tables) |
| `NDMC Talent Search Exam (NSTSE) Analysis Dashboard.pbix` | Full Power BI dashboard |
| `NSTSE_Dashboard.pdf` | Exported static view of the dashboard |
| `README.md` | Project documentation for GitHub |

---

## 🚀 How to Use

1. Download the `.pbix` file
2. Open it in Power BI Desktop
3. Explore and interact with filters and visuals
4. Customize visuals or add new measures for practice

---

## 🧑‍💼 About Me

I currently work at **NDMC HQ** supporting the Education Department. I specialize in educational data analysis and developed this project as part of my career transition portfolio to **Data Analyst roles** in the private sector.

---

## 📬 Contact

If you’re a recruiter or collaborator, feel free to reach out on:
- [LinkedIn](#) https://in.linkedin.com/in/lochansinghal

---

⭐ **Star this repo** if you found it helpful!
