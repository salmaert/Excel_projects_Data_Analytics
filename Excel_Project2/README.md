# 📊 Project 2 – Data Skills Salary Dashboard  

## 📌 Overview  
This project explores the relationship between **skills, job roles, and salaries** in the data industry.  
Using **Power Query, Power Pivot, and advanced Excel features**, the goal is to uncover which skills are most in demand and how they impact pay across different regions.  

---

## ❓ Objectives  
The analysis focused on four main questions:  
1. Do professionals with more technical skills earn higher salaries?  
2. How do salaries compare between the United States and other countries?  
3. Which technical skills are most frequently required in data-related job postings?  
4. What are the top 10 skills that lead to the highest salaries?  

---

## 🛠️ Excel Techniques Applied  
- **Power Query** → cleaned, transformed, and reshaped raw job data.  
- **Power Pivot** → built relationships between job postings and associated skills.  
- **DAX formulas** → created custom measures such as median salary.  
- **PivotTables** → aggregated job and salary information.  
- **Charts & Combo Charts** → visualized salary trends and skill demand.  

---

## 📂 Dataset  
The dataset contains job postings from 2023 with details on:  
- Job titles  
- Salary information  
- Geographic location (US vs Non-US)  
- Technical skills required  

---

## 🔹 What are the top skills of data professionals?  
  

💪 **Process**  
- After cleaning the dataset in **Power Query**, I loaded the data into **Power Pivot**.  
- Integrated two tables:  
  - **data_jobs_salary** → job titles, salaries, and countries.
  <img width="959" height="330" alt="Project_2 5" src="https://github.com/user-attachments/assets/88f4ed3d-644d-42d9-a26a-f74bb8024c25" />
 
  - **data_jobs_skill** → skills linked to each job via `job_id`.
   <img width="593" height="338" alt="project_2 6" src="https://github.com/user-attachments/assets/bfd6ec69-2808-4ecd-862c-3b9b150f79d4" />

- Built a **relationship on `job_id`** to connect jobs with their required skills.
 <img width="863" height="340" alt="Project_2 4" src="https://github.com/user-attachments/assets/2e72821b-83c6-49e1-acd4-e2a9ab88764b" />

- Used the **Power Pivot menu** to refine the data model and create measures.  

📊 **Analysis**  
- **SQL** and **Python** dominate as the top skills in data-related jobs, confirming their foundational role in analytics.  
- **AWS** and **Azure** also stand out, reflecting the industry’s growing shift toward cloud services and big data platforms.
  
  <img width="738" height="191" alt="Project_2 1" src="https://github.com/user-attachments/assets/23dabb64-8a02-404b-b31b-3b275da42f57" /> 

💡 **Insights**  
- Core skills like SQL and Python remain essential across the market.  
- Cloud technologies are rapidly increasing in importance and create opportunities for higher-paying positions.  

🤔 **So What**  
Identifying the most in-demand skills helps professionals stay competitive and directs training or education programs toward the **most impactful technologies**.  

---

### 2️⃣ Salary by Region  
🧮 **DAX Measures**  
```DAX
Median Salary :=
MEDIAN ( data_jobs_all[salary_year_avg] )

Median Salary US :=
CALCULATE (
    MEDIAN ( data_jobs_all[salary_year_avg] ),
    data_jobs_all[job_country] = "United States"
)

Median Salary Non-US :=
CALCULATE (
    [Median Salary],
    data_jobs_all[job_country] <> "United States"
)
```
📊 **Analysis**  
- Senior roles such as **Data Scientist** and **Senior Data Engineer** command higher salaries in both US and Non-US markets.  
- Salaries in the **US** are consistently higher, especially in technical roles.  

💡 **Insights**  
- High-level expertise is rewarded worldwide.  
- US jobs offer a clear salary premium, reflecting the concentration of the tech industry.  


<img width="846" height="181" alt="Project_2 2" src="https://github.com/user-attachments/assets/850bad3b-b87b-40dd-a33a-5ac480cca1d5" />

🤔 **So What**  
- **Job seekers** can set realistic salary expectations by region.  
- **Employers** can align compensation with global benchmarks. 

---
## 🔹 What’s the pay of the top 10 skills?  

💪 **Process**  
The chart shows the **median salary for the top 10 skills** (bars) compared with how often each skill appears in job postings (line).  

📊 **Analysis**  
- **MongoDB** has the highest median salary (~$197K).  
- **Java** and **Spark** also show strong pay potential.  
- **Python** and **SQL** are the most common but tied to moderate salaries.  
- Cloud skills (**AWS, GCP, Azure**) sit in the mid-high range.  

💡 **Insights**  
- Specialized tools = higher salaries.  
- Core skills are essential but not the top-paying.  
- Cloud skills balance demand with good compensation.

<img width="908" height="224" alt="Project_2 3" src="https://github.com/user-attachments/assets/02008643-3f9f-467c-a523-86999fa90210" /> 

🤔 **So What**  
- Professionals should mix **core (Python, SQL)** with **niche/cloud (MongoDB, Spark, AWS)**.  
- Employers can use this to identify which skills justify higher pay.

---

## 🧑‍💻 Skills Demonstrated  
- Data preparation and cleaning with **Power Query**  
- Data modeling with **Power Pivot**  
- Calculations using **DAX**  
- Salary and skill insights via **PivotTables & Charts**  
- Full Excel-based dashboard creation  

---

## 📜 Conclusion  
This project demonstrates how Excel can be leveraged for end-to-end data analysis, from cleaning and modeling to advanced reporting.  
The findings confirm that **diverse technical skills directly contribute to higher salaries**, while also showing how geography influences pay.  

👉 For data professionals, this highlights the importance of investing in **high-value skills like SQL, Python, and cloud platforms** to stay competitive in the job market.  

