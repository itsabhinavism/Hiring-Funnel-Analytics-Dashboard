# Hiring Funnel Analytics Dashboard (Power BI) 🚀

A Power BI dashboard that turns raw job-posting + skills data into a **clear “hiring funnel” view** of the market:  
**What roles are in demand, which skills dominate those roles, and what the salary reality looks like** (hourly + yearly).

This project is designed to help recruiters, hiring managers, and candidates answer questions like:
- **Which job titles have the most openings?**
- **Which skills are most frequently required across roles?**
- **How do salaries compare across job titles and countries?**
- **What happens when we filter by role (e.g., Data Analyst vs Data Engineer) or by geography?**

---

## Dashboard Preview 🖼️

- `filtered.png`  

Example markdown embed:
```md
![Hiring Funnel Dashboard Overview](images/dashboard_overview.pdf)
```

---

## Key Highlights (What this dashboard delivers) ✅

### 1) Market Snapshot in One Screen
The top KPI cards provide an instant overview:
- **Job Count:** ~**13K** openings (high-volume dataset)
- **Skills per Job:** ~**5.8** (skill breadth demanded per role)
- **Median Hourly Salary:** ~**$61** (overall benchmark)

These KPIs make it easy to **set expectations quickly** before drilling deeper.

---

### 2) Skill Popularity (What companies want most) 🔥
The *Skill Popularity* bar chart ranks the most requested skills across the dataset.  
From the report view, the most visible skills include:
- **Python**
- **SQL**
- **AWS**
- **Azure**
- **Tableau**
- **Spark**
- **R**
- **Excel**
- **Power BI**

This is extremely useful for:
- Candidates → prioritizing learning
- Recruiters → writing targeted job descriptions
- Hiring teams → identifying realistic “must-haves” vs “nice-to-haves”

---

### 3) Salary Benchmarks by Role 💰
The *Job Salaries* visual compares **Median Yearly Salary** across job titles (and supports slicing).

This helps answer:
- Which roles command the highest pay?
- Which roles are high-volume but underpaid?
- How salary shifts when filtering by **Country** or **Job Title**

---

## Interactivity (Slicers & Controls) 🎛️

The dashboard is built for exploration with slicers:
- **Select Job Title** (examples visible: Business Analyst, Cloud Engineer, Data Analyst, Data Engineer, …)
- **Select Country**
- **Clear Slicers** button for quick reset

This design lets a reviewer instantly test scenarios like:
- “What’s the salary for **Data Engineer** roles in a specific country?”
- “Which skills are most associated with **Data Analyst** roles?”
- “How does job share change when I focus on one category?”

---

## Data Model (Star Schema) 🧠

The report follows a clean dimensional model (as seen in the Fields pane):

### Fact Table
- **`job_postings_fact`**
  - key fields seen: `job_id`, `company_id`, `job_title`, `job_title_short`, `job_country`, `job_location`, etc.
  - salary metrics seen: `salary_hour_avg`, `salary_year_avg` (plus related salary fields)

### Dimension Tables
- **`company_dim`** (company attributes)
- **`date_dim`** (time intelligence)
- **`skills_dim`** and related skill mapping tables (skill intelligence)
- **`schedule_dim`** (schedule/shift / job schedule context)

This structure makes the report:
- scalable (easy to add more measures)
- fast to slice/filter
- consistent for analytics and storytelling

---

## Measures & Metrics (What’s calculated) 📌

The report uses a measures layer (visible as **Measures**) to compute:
- **Job Count**
- **Skills per Job**
- **Median Hourly Salary**
- **Median Yearly Salary**
- Skill-based metrics used in the “Skill Popularity” view (e.g., skill count / job percent style measures)

These measures make the dashboard **dynamic**—they recalculate instantly based on slicers.

---

## How to Use (For a Hiring Manager / Recruiter) 🧩

1. Open the PBIX in Power BI Desktop  
2. Start with **All** job titles and countries (default view)  
3. Choose a **Job Title** to see:
   - most demanded skills for that role
   - salary distribution/benchmarking
4. Choose a **Country** to compare regional trends  
5. Use **Clear Slicers** to restart exploration

---

## Tools & Skills Demonstrated 🛠️

- **Power BI Desktop** (data modeling + interactive reporting)
- **Star schema modeling** (fact/dim approach)
- **DAX measures** for dynamic KPIs
- **Analytics storytelling** (KPIs → breakdowns → drilldown exploration)
- **Recruiting analytics mindset** (turning job + skills data into hiring decisions)

---

## Repository Structure 📁

Suggested structure (matches typical BI portfolio repos):

```
Hiring-Funnel-Analytics-Dashboard/
├─ Hiring Funnel Analytics Dashboard.pbix
├─ Hiring Funnel Analytics Dashboard.pdf
├─ images/
│  ├─ dashboard_overview.png
│  ├─ skill_popularity.png
│  └─ job_salaries.png
└─ README.md
```

---

## About Me 👤
If you’re reviewing this as part of my portfolio:  
I focus on building dashboards that are not just visually clean, but also **decision-ready**—with a strong data model, meaningful KPIs, and intuitive interactivity.

If you'd like, I can also add:
- a **“Hiring Funnel Insights” page** with executive summary cards  
- a **Role vs Skill matrix** (heatmap style)  
- a **geo salary comparison** map visualization  

---

### ⭐ If you find this useful, please consider starring the repo!
