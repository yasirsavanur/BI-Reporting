# Stack Overflow Developer Survey 2019 – Technology Trends & Analysis

This project analyses the **2019 Stack Overflow Developer Survey** to understand technology trends in programming languages, databases, platforms, and developer demographics. The goal was to build an end‑to‑end pipeline: collect data, clean it, analyse it, and present the results in an interactive dashboard using **IBM Cognos Dashboard Embedded (CDE)**. The same dashboard was created using [Tableau](https://public.tableau.com/app/profile/yasir.savanur/viz/StackOverflowDeveloperSurvey2019-Visualization_16880126654310/FutureTechTrends) as well.

The [dataset](https://stackoverflow.blog/2019/04/09/the-2019-stack-overflow-developer-survey-results-are-in/) comes from the official survey results, but for this project I worked with a modified subset to keep the scope manageable.

---

## Dashboard Overview

The dashboard is divided into three main sections:

### Current Technology Usage
- Top 10 programming languages  
- Top 10 databases  
- Platforms developers work with  
- Top 10 web frameworks  

### Future Technology Trends
- Top 10 languages developers want to learn next year  
- Top 10 databases developers want to learn next year  
- Desired platforms for the next year  
- Top 10 web frameworks developers want to learn next year  

### Demographics
- Respondents by gender  
- Respondents by country  
- Respondents by age  
- Education level split by gender  

---

## End‑to‑End Workflow

This project covers the full data science workflow:

1. **Collecting_job_data_using_APIs.ipynb**  
   Pulled job data using APIs to connect survey results with real‑world demand. Automated collection ensured consistency and avoided manual downloads.

2. **Web_Scraping.ipynb**  
   Scraped additional information from websites to enrich the dataset. This added industry context beyond the survey.

3. **Explore_Dataset.ipynb**  
   Performed an initial exploration of the dataset. Checked column names, variable meanings, missing values, and inconsistencies.

4. **Data_Wrangling.ipynb**  
   Cleaned and reshaped the dataset. Tasks included handling missing values, normalizing text entries, and restructuring tables for easier analysis.

5. **Exploratory_Data_Analysis.ipynb**  
   Investigated distributions, correlations, and demographic splits. This step helped identify emerging trends and patterns.

6. **Data_Visualisation.ipynb**  
   Created charts and plots to make findings easier to interpret. Visualisations included bar charts, pie charts, and trend lines.

7. **Technology Trends & Analysis Presentation.pdf / .pptx**  
   Summarised the key findings and implications in a presentation format. Designed for HR and IT heads to understand skill requirements and plan for the future.

---

## Key Takeaways

- JavaScript, HTML/CSS, and SQL were the top languages in 2019, but Python and TypeScript were quickly rising.  
- MySQL was the most popular database, while MongoDB, Redis, and Elasticsearch were gaining traction.  
- Platforms like Docker and AWS were becoming essential for modern development.  
- There was a noticeable gender gap and uneven distribution of tech adoption across countries.  
- Companies need to adapt quickly to changing technology trends and address demographic and geographic gaps.

---

## Purpose

The main goal was to practice the full data science workflow: collecting data, cleaning it, analysing it, and presenting it in a professional way. The dashboards make the results interactive and easier to explore, providing a snapshot of how fast technology changes and what skills companies might be looking for in the near future.
