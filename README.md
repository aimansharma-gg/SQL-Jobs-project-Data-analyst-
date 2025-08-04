Data Analytics Jobs in Atlanta – Insights
This project analyzes the job market for Data Analyst roles located in Atlanta, GA, using 2023 job postings data. It combines SQL-driven data extraction with interactive Power BI visualizations to uncover key insights about demand, salaries, skills, and top-paying companies.

⚠️ Data Source Notice:
All job posting data used in this project was collected by Luke Barousse in 2023.
Visit his website and dataset here: lukebarousse.com/sql

📁 Files
DATA_ANALYTICS_JOBS_IN_ATLANTA_INSITES.pbix: Power BI report file containing dashboards and visualizations based on SQL queries.

SQL scripts: Used to query and join job posting and skills data for analysis.

🔍 Objectives
Identify the most in-demand technical skills for Data Analyst roles in Atlanta.

Highlight the top-paying job postings and associated skills.

Provide a clear view of salary distributions for Data Analyst roles in Atlanta.

Help aspiring analysts align their skillsets with market demands.

🧠 Data Sources
job_postings_fact: Contains job posting details including title, location, and salary.

skills_dim, skills_job_dim: Define skills associated with each job.

company_dim: Contains company names and metadata.

🛠️ SQL Queries Overview
1. Top 10 In-Demand Skills for Data Analysts in Atlanta
sql
Copy
Edit
SELECT 
    skills,
    COUNT(skills_job_dim.job_id) AS demand_count
...
LIMIT 10;
Purpose: Ranks skills by frequency in job postings.

Power BI Visual: Bar chart of top 10 skills by demand.

2. Top Paying Data Analyst Jobs (with Skills)
sql
Copy
Edit
WITH top_paying_jobs AS (
    SELECT ...
)
SELECT 
    top_paying_jobs.*, skills
...
ORDER BY salary_year_avg DESC;
Purpose: Merges job info with skill data to display high-paying roles.

Power BI Visual: Table of top salaries with associated skillsets.

3. General Salary Overview
sql
Copy
Edit
SELECT
    job_id,
    job_title_short,
    job_location,
    salary_year_avg,
    ...
ORDER BY salary_year_avg DESC;
Purpose: Retrieves and ranks salaries for all Data Analyst roles.

Power BI Visual: Boxplot or histogram for salary distribution.

📈 Power BI Dashboard Highlights
Top Skills by Demand: A clear breakdown of the most requested skills like SQL, Excel, Python, Tableau, etc.

Salary Explorer: Interactive table for top-paying jobs and employers.

Skill–Salary Mapping: See what skills are common among higher-paying roles.

Location Filter: All visuals filtered for Atlanta, GA.

💡 Key Insights
💼 SQL, Excel, and Python dominate the skill requirements.

🏢 Top-paying companies include well-known firms in tech, consulting, and finance.

💰 Salaries for Data Analyst roles in Atlanta vary significantly, often depending on skillset and company.


👨‍💻 Author
Aiman Sharma
Undergraduate Industrial Engineering Student @ Georgia Tech
Interested in Data Analytics, Operations Research, and Supply Chain
GitHub: aimansharma-gg

