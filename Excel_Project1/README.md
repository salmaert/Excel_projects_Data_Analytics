# 📊 Data Science Salary Calculator  

## Introduction
This Excel Salary Dashboard was created to help job seekers analyze salaries for various data-related jobs. It allows users to explore whether they are being adequately compensated and to understand how job title, location, and required skills impact salaries.

![image alt](https://github.com/salmaert/Excel_projects_Data_Analytics/blob/ea926ab0d06a1d9bb42dde232b7d79eeed15343e/Excel_Project1/Project1_image.png)

The data used comes from an Excel course dataset, which includes real-world 2023 data science job information with details on job titles, salaries, locations, and essential skills.

**Dashboard File:** [1_Salary_Dashboard.xlsx](#)  

**Excel Skills Used:**
- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation

---

## Dataset
The dataset contains detailed information for data science jobs, including:
- 👨‍💼 Job Titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

---

## Dashboard Components

### 1. Data Organization
- Sorted job titles by descending salary to highlight higher-paying roles.
- Structured dataset for clear analysis of job title, country, salary, schedule type, and skills.

**Learning Outcomes:**
- How to structure and organize data for analysis.
- Recognized salary trends, e.g., senior roles and engineers earn more than analyst roles.

---

### 2. Charts

#### a. Data Science Job Salaries – Bar Chart
- **Excel Features:** Horizontal bar chart, formatted salary values, optimized layout.
- **Design Choice:** Horizontal bars for visual comparison of median salaries.
- **Insights:** Quickly identifies salary trends and highlights higher-paying positions.

<img width="464" height="244" alt="image" src="https://github.com/user-attachments/assets/69cd72c7-a56b-410d-85c2-750184fdb360" />

### Formulas & Functions

####  Median Salary by Job Title
```excel
=MEDIAN(
    IF(
        (jobs[job_title_short]=A2)*
        (jobs[job_country]=country)*
        (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
        (jobs[salary_year_avg]<>0),
        jobs[salary_year_avg]
    )
)
```


#### b. Country Median Salaries – Map Chart
- **Excel Features:** Map chart to plot median salaries globally.
- **Design Choice:** Color-coded map for visual differentiation of salary levels by region.
- **Insights:** Understand geographic salary disparities and highlight high/low-paying regions.
  
![imagealt](https://github.com/salmaert/Excel_projects_Data_Analytics/blob/61594dcd3db7aadbb766505cbb686c57c9310f5a/Excel_Project1/Project_1.2.png)

## KPI Section – Median Salary • Jobs Source • Count Salary  

![imagealt](https://github.com/salmaert/Excel_projects_Data_Analytics/blob/287863c3b570d3b0d459faa5c21187ba6f6258fa/Excel_Project1/Project_1.3.png)

🛠️ **Excel Features:** KPI cards update automatically when filters are applied.  
📊 **Displayed Metrics:**  
- **Median Salary** – central value of salaries for the selected role, country, and type.  
- **Jobs via** – shows the main job platform used, based on role and country (e.g., Ai-Jobs.net).  
- **Count Salary** – number of jobs available for the selected Job Title, Country, and Work Type.
- 💡**Insights Gained:** Provides users with quick, reliable context on salary levels, job availability, and the most relevant job source for the selected filters.  

---

## 🛠️ Tools & Skills  
- Advanced **Excel formulas** for multi-criteria filtering and calculations  
- **Dynamic charts** for interactive data visualization  
- **KPI dashboards** for at-a-glance decision making  

---

## 📜 Conclusion  
This dashboard was built to showcase insights into salary trends across various data-related job titles.  
It demonstrates how location and work type influence salary levels and helps users make informed career decisions.  


