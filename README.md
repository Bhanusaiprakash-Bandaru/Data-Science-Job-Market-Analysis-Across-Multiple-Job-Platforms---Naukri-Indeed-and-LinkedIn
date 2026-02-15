![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-EDA-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

# 📊 Project Observations – Step-by-Step Explanation (Data-Driven)

## 1️⃣ Data Collection (Web Scraping)

Real-time job posting data was collected from three major job portals:
- Naukri
- Indeed
- LinkedIn

Each portal was scraped independently using automated scripts, and the data was later merged into a single dataset.

### 🔍 Observation
- Each portal shows different posting volumes and formats.
- Job titles, skills, and salary details are not standardized.
- Salary information is frequently missing, especially on LinkedIn.

This confirms that raw job market data is **unstructured and inconsistent**, and cannot be analyzed directly.

---

## 2️⃣ Data Merging

All three datasets were merged into one consolidated dataset.
A new column (`Job_Site_Name`) was added to identify the source portal.

### 🔍 Observation
- Job posting volume varies significantly across portals.
- Dataset sizes do not need to be equal for merging.
- Duplicate and noisy records became more visible after merging.

This created a **single source of truth** for analysis.

---

## 3️⃣ Data Understanding (Initial Exploration)

The dataset was examined for:
- Shape and structure
- Column data types
- Missing values
- Duplicate records
- Unique roles, locations, companies, and skills

### 🔍 Observation
- High missing values in `Salary` and `Skills`.
- Masked values such as “****” and “Not Available”.
- Same job roles and cities appeared in multiple formats.

This shows that **understanding the data must come before visualization or modeling**.

---

## 4️⃣ Data Cleaning & Feature Engineering

To make the data usable:

### ✔ Handling Missing and Invalid Values
- Invalid salary values were converted to `NaN`.
- A new column `Salary_Disclosed` was created to track transparency.

### ✔ Role & Experience Standardization
- Job titles were grouped into:
  - Data Scientist
  - Data Analyst
  - ML Engineer
  - Other
- Experience was categorized into:
  - Entry (0–2 yrs)
  - Early (3–5 yrs)
  - Mid (6–9 yrs)
  - Senior (10+ yrs)

### ✔ Location & Skills Processing
- City was extracted from raw location text.
- Skills were cleaned and standardized.

### 🔍 Observation
- Grouping reduced noise and exposed clear hiring patterns.
- Raw job titles are too granular to analyze directly.

---

## 5️⃣ Summary-Level Insights (Before Visualization)

Key summary tables revealed:
- Bengaluru and Hyderabad dominate job postings.
- A small number of companies post a large share of jobs.
- Python, Machine Learning, SQL, and Data Analytics appear most frequently.
- Most job postings are recent, indicating an active market.

This validated **which variables are meaningful to visualize**.

---

## 6️⃣ Univariate Exploratory Data Analysis (EDA)

Single-variable analysis showed:

### ✔ Job Roles
- Data Scientist and Data Analyst roles dominate.
- ML Engineer roles are fewer but specialized.

### ✔ Experience Levels
- Majority of jobs target entry and early-career professionals.
- Senior roles are limited and selective.

### ✔ Skills
- Python is the most demanded skill.
- ML, SQL, and analytics consistently appear across roles.

### 🔍 Observation
Univariate analysis answers **“what is common”**, but not **“why it happens”**.

---

## 7️⃣ Bivariate Exploratory Data Analysis

Relationships between variables revealed deeper insights:

### ✔ Role × Job Portal
- LinkedIn favors specialized and senior roles.
- Naukri and Indeed show more entry and analyst roles.

### ✔ Role × Salary Disclosure
- Entry and analyst roles disclose salary more often.
- Senior and specialized roles hide salary frequently.

### ✔ Role × Location
- Advanced roles cluster in tech hubs like Bengaluru and Hyderabad.

### 🔍 Observation
Bivariate analysis exposes **business behavior**, not just counts.

---

## 8️⃣ Hypothesis Testing (Statistical Validation)

Chi-square tests confirmed that:
- Salary disclosure depends on job role.
- Skill demand varies by role.
- Job location depends on role.
- Salary disclosure depends on experience level.

### 🔍 Observation
All results were statistically significant.  
The patterns seen in charts are **not random**.

---

## 🎯 Final Takeaway – Addressing Ramesh’s Confusion (Data-Driven)

Ramesh is a non-IT professional trying to enter the data science field.  
By looking at individual job portals, he faced confusion.  
This project replaces assumptions with evidence.

### ❓ Ramesh’s Questions → ✅ Data-Backed Answers

- **Which roles are actually in demand?**  
  → Data Scientist and Data Analyst roles have the highest demand across portals.

- **Is the market entry-level friendly?**  
  → Yes. Most postings target entry and early-career professionals.

- **Which skills should he learn first?**  
  → Python, Machine Learning, SQL, and Data Analytics are non-negotiable.

- **Which cities offer more opportunities?**  
  → Bengaluru and Hyderabad dominate data science hiring.

- **Can he rely on salary information?**  
  → No. Most companies do not disclose salary, especially for senior roles.

- **Does one job portal show the full picture?**  
  → No. Each portal highlights different hiring patterns.

---

### ✅ How This Project Helps Ramesh

Instead of guessing based on one portal:
- Ramesh sees **true role demand** across platforms.
- He knows **which skills give the highest ROI**.
- He can **target the right cities**.
- He understands **salary transparency limitations**.
- He can plan his career **strategically, not emotionally**.

This project turns scattered job postings into **actionable career intelligence**.
