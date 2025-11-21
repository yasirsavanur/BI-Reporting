# Stack Overflow Developer Survey 2019 – Technology Trends & BI Reporting

This project looks at the **2019 Stack Overflow Developer Survey** to understand what technologies developers were using in 2019 and what they wanted to learn next. I also bring in job‑market signals (GitHub Jobs API) and a small web‑scraped dataset to compare survey trends with real hiring demand.

The end result is a simple BI‑style report and dashboard (see the slides / PDF in this repo).

---

## Objectives

- Collect job‑market data using APIs and basic web scraping.
- Clean and wrangle the survey dataset into a usable format.
- Explore the data with EDA to find patterns and gaps.
- Build visualisations that answer “what’s popular now vs next.”
- Summarise findings in a BI report/dashboard.

---

## Data Sources

1. **Stack Overflow Developer Survey 2019 (subset)**  
   A cleaned subset of the public 2019 survey. It includes:
   - Technologies worked with and desired next year  
     (languages, databases, platforms, web frameworks)
   - Demographics  
     (age, gender, education, country, etc.)

   Files used here:
   - [`Dataset/m5_survey_data_technologies_normalised.csv`](Dataset/m5_survey_data_technologies_normalised.csv)
   - [`Dataset/m5_survey_data_demographics.csv`](Dataset/m5_survey_data_demographics.csv)
   - [`Dataset/m4_survey_data.sqlite.zip`](Dataset/m4_survey_data.sqlite.zip)

2. **GitHub Jobs API (job demand snapshot)**  
   Used to count how many jobs mention certain technologies.

3. **Web‑scraped list of popular programming languages**  
   A small scrape to practice extraction + saving results to CSV.

---

## Project Workflow

This repo follows a full mini data‑science / BI pipeline:

1. **Collecting job data through APIs**  
   Notebook: [`1. Collecting_job_data_using_APIs.ipynb`](1.%20Collecting_job_data_using_APIs.ipynb)  
   - Pulls job listings from the GitHub Jobs API  
   - Counts demand for specific technologies  
   - Saves results into a spreadsheet

2. **Collecting extra data through web scraping**  
   Notebook: [`2a. Web_Scraping.ipynb`](2a.%20Web_Scraping.ipynb)  
   - Scrapes a public webpage listing popular languages  
   - Stores results in a CSV for comparison

3. **Survey dataset exploration**  
   Notebook: [`2b. Explore_Dataset.ipynb`](2b.%20Explore_Dataset.ipynb)  
   - Loads the survey data  
   - Checks shape, data types, missing values, duplicates

4. **Data wrangling**  
   Notebook: [`3. Data_Wrangling.ipynb`](3.%20Data_Wrangling.ipynb)  
   - Removes duplicates and irrelevant columns  
   - Handles missing data  
   - Normalises multi‑select columns (e.g., multiple languages per respondent)

5. **Exploratory data analysis**  
   Notebook: [`4. Exploratory_Data_Analysis.ipynb`](4.%20Exploratory_Data_Analysis.ipynb)  
   - Looks for distributions and relationships  
   - Aggregates counts for “worked with” vs “desired next year”

6. **Data visualisation + BI reporting**  
   Notebook: [`5. Data_Visualization.ipynb`](5.%20Data_Visualization.ipynb)  
   - Builds charts for technology usage, trends, and demographics  
   - Output is summarised into a BI report / dashboard:
     - [`Technology Trends & Analysis Presentation.pptx`](Technology%20Trends%20%26%20Analysis%20Presentation.pptx)
     - [`Technology Trends & Analysis Presentation.pdf`](Technology%20Trends%20%26%20Analysis%20Presentation.pdf)

---

## Key Findings (from the survey subset)

### Current technology usage (2019)

**Top languages developers worked with**
1. JavaScript  
2. HTML/CSS  
3. SQL  
4. Bash/Shell/PowerShell  
5. Python  
6. Java  
7. C#  
8. TypeScript  
9. PHP  
10. C++

**Top databases developers worked with**
1. MySQL  
2. Microsoft SQL Server  
3. PostgreSQL  
4. SQLite  
5. MongoDB  
6. Redis  
7. Elasticsearch  
8. Oracle  
9. MariaDB  
10. Firebase

**Top platforms developers worked with**
1. Linux  
2. Windows  
3. Docker  
4. AWS  
5. Slack  
6. MacOS  
7. Android  
8. Microsoft Azure  
9. Raspberry Pi  
10. WordPress

**Top web frameworks developers worked with**
1. jQuery  
2. Angular / Angular.js  
3. React.js  
4. ASP.NET  
5. Express  
6. Spring  
7. Vue.js  
8. Flask  
9. Django  
10. Laravel

---

### Future technology trends (what people wanted next)

**Top languages developers wanted to learn next**
1. JavaScript  
2. HTML/CSS  
3. Python  
4. SQL  
5. TypeScript  
6. C#  
7. Bash/Shell/PowerShell  
8. Java  
9. Go  
10. Kotlin  

Big takeaway: Python, TypeScript, Go, and Kotlin were climbing fast even if they weren’t top‑3 in current use.

**Top databases developers wanted next**
1. PostgreSQL  
2. MongoDB  
3. Redis  
4. MySQL  
5. Elasticsearch  
6. Microsoft SQL Server  
7. SQLite  
8. Firebase  
9. MariaDB  
10. DynamoDB  

Big takeaway: PostgreSQL and modern NoSQL/fast‑cache tools were clearly gaining momentum.

**Top platforms developers wanted next**
1. Linux  
2. Docker  
3. AWS  
4. Windows  
5. Android  
6. Kubernetes  
7. MacOS  
8. Raspberry Pi  
9. Google Cloud Platform  
10. Slack  

Big takeaway: Docker + Kubernetes interest shows how strongly cloud‑native dev was taking over.

**Top web frameworks developers wanted next**
1. React.js  
2. Vue.js  
3. Angular / Angular.js  
4. ASP.NET  
5. jQuery  
6. Express  
7. Spring  
8. Django  
9. Flask  
10. Ruby on Rails  

Big takeaway: React and Vue were the main “next‑step” frameworks people were aiming for.

---

### Demographics snapshot

- **Gender split is heavily uneven** in this subset:  
  - “Man” respondents dominate by a lot, with “Woman” and non‑binary groups much smaller.  
- **Average respondent age is about 31**, and the median is 29.  
- **Top countries represented**: United States, India, United Kingdom, Germany, Canada.  
- **Education level**: most respondents report a Bachelor’s degree, followed by Master’s degrees.

---

## How to Run

This project is notebook‑based. Open the `.ipynb` files in Jupyter Lab / VS Code.  
Main libraries used: `pandas`, `numpy`, `matplotlib`, `seaborn`, `requests`, `beautifulsoup4`.

Example install:

```bash
pip install pandas numpy matplotlib seaborn requests beautifulsoup4
```

---

## Deliverables

- Cleaned and normalised survey datasets (CSV + SQLite)
- EDA + visualisation notebooks
- BI dashboard summary in slides/PDF:
  - [`Technology Trends & Analysis Presentation.pdf`](Technology%20Trends%20%26%20Analysis%20Presentation.pdf)

---

## Possible Extensions

- Add 2020–2024 survey years to show trend direction over time.
- Compare survey popularity with job‑market popularity more formally.
- Turn the dashboard into a live Power BI / Tableau / Dash app.
- Segment trends by role (student vs professional, backend vs frontend, etc.).

---

## Author

**Yasir Savanur**  
LinkedIn: https://www.linkedin.com/in/yasir-savanur/
