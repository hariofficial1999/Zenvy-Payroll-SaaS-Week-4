# 🚀 Zenvy Payroll SaaS: Core Payroll Module & Data Engineering

Welcome to the **Zenvy Payroll SaaS** project. This repository contains the complete data engineering pipeline for a modern Payroll SaaS platform, focusing on data cleaning, feature engineering, MySQL migration, and professional business intelligence dashboarding.

---

## 📂 Project Overview
This project was developed during **Week 4** of the internship to demonstrate advanced data engineering techniques on payroll datasets. The pipeline transforms raw, fragmented data into actionable insights for HR and Finance departments.

### 🛠️ Tech Stack
- **Language:** Python 3.12
- **Libraries:** Pandas, NumPy, Plotly, Seaborn, Matplotlib, SQLAlchemy, PyMySQL
- **Database:** MySQL
- **BI Tools:** Power BI
- **Environment:** Jupyter Notebook

---

## 📊 Pipeline Stages

### 1. Data Setup & Ingestion
Merging multiple datasets (`Employees`, `Payroll`, and `Attendance`) into a unified master record using unique `employee_id` identifiers.

### 2. Preprocessing & Cleaning
- **Normalization:** Stripping whitespace and standardizing casing for categorical fields like `Department` and `Designation`.
- **Type Conversion:** Ensuring financial columns (`gross_salary`, `tax_deduction`) are correctly typed as numeric to prevent calculation errors.
- **Handling Missing Data:** Detecting and resolving null values and duplicates.

### 3. Feature Engineering
Creating high-value business metrics:
- **Time-based Features:** Extracting Joining Day, Month, Quarter, and Year.
- **KPI Metrics:** Percentage-based overtime impact, net salary calculations, and department-wise cost analysis.

### 4. Exploratory Data Analysis (EDA)
Comprehensive visualizations to uncover trends:
- **Departmental Expense Distribution:** Understanding where payroll costs are highest.
- **Salary Trends:** Analyzing salary bands across designations.
- **Overtime Impact:** Interactive widgets to filter and view overtime costs by department.

### 5. MySQL Migration
Automated migration of processed DataFrames to a **MySQL** database (`zenvy_payroll`) using SQLAlchemy. This ensures data is ready for enterprise-level querying and persistence.
- **Tables Created:** `employees`, `payroll`, `attendance`, `master_payroll_record`.

### 6. Power BI Integration
Designing a professional 2-page dashboard:
- **Executive Summary:** High-level KPIs (Total Cost, Attendance Avg, Headcount).
- **Department Analysis:** Deep-dive into specific department performance and cost breakdowns.

---

## 📁 File Structure
| File | Description |
| :--- | :--- |
| `TEST.ipynb` | Main Python notebook with the full engineering/analysis pipeline. |
| `zenvy_employees.csv` | Raw employee records. |
| `zenvy_payroll.csv` | Raw payroll records. |
| `zenvy_attendance.csv` | Raw attendance records. |
| `zenvy_master_for_powerbi.csv` | **Primary Export:** Cleaned & engineered dataset for BI tools. |
| `power bi.pbix` | Power BI dashboard file. |
| `Zenvy_Final_Report.pdf` | Final summary report of project findings. |

---

## 🚀 How to Run
1.  **Clone the Repo:**
    ```bash
    git clone https://github.com/your-repo/zenvy-payroll-saas.git
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas numpy plotly seaborn matplotlib sqlalchemy pymysql
    ```
3.  **Run the Notebook:**
    Launch `TEST.ipynb` in Jupyter or VS Code.
4.  **Database Connection:**
    Ensure a local MySQL instance is running. Update the connection string in **Step 7** of the notebook with your credentials.

---

## 🏆 Key Achievements
- Built a robust, reusable data engineering pipeline.
- Automated data migration to a relational database.
- Created interactive dashboards for executive decision-making.
- Generated comprehensive PDF reporting for stakeholders.

---


