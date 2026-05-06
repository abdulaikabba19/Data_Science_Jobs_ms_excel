## DATA SCIENCE JOBS DASHBOARD
**Introduction and Overview**

This project is about creating a clear view about data-related jobs and their respective median salaries. This is a real world data that was gathered by Luke Barousse and Kelly Adams. Attached to this project is a link to their YouTube channel: 
[luke's_channel_for_excel](https://youtu.be/pCJ15nGFgVg?si=CK-Ns5S53P6KFAsk). 

This dataset used for this project contains real-world data science job information from 2023, and it include various job titles, locations, salary, and key skills that one may consider when wanting to go into the world of data science. 

The completed version of this project and how it works is illustrated below: 
![data_science_dashboard](https://github.com/abdulaikabba19/Data_Science_Jobs_ms_excel/blob/main/images_data_jobs/dashboard%20gif.gif?raw=true)

## 🔎 Skills Used During Project
During the process of completing this project, I was able to intensely learn, and not limited to:

**📉 Charts creation**

**🧮 Formulas and Functions(simple and advanced)**

**✅ Data Validation**

## 📑 Main Insights

**⭐1. Data-Science Jobs and salaries Trend**
**Key Insights**
- **Senior technical roles dominate compensation**, with Senior Data Scientist, Machine Learning Engineer, and Senior Data Engineer consistently appearing at the top of the salary range, all clustering around the $150K–$155K mark.

- **Data-focused** roles show a clear progression path, where entry-level positions like **Data Analyst and Business Analyst** sit around $90K, while advanced roles such as **Data Scientist and Data Engineer** rise into the $110K–$130K range, highlighting strong salary growth with specialization.

- **Engineering and cloud roles** remain highly competitive, with Software Engineer and Cloud Engineer salaries ranging from $115K–$150K, reflecting the increasing demand for hybrid data–engineering skill sets across the industry.

The formula used to get the results of the aforementioned is:
```
=MEDIAN(
IF((jobs[job_title_short]=A3)*
(jobs[salary_year_avg]<>0)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))
,jobs[salary_year_avg]))
```
![job_title_salary](https://github.com/abdulaikabba19/Data_Science_Jobs_ms_excel/blob/main/images_data_jobs/job%20title%20gif.gif?raw=true)
*This bar chart was created using the key insights and calculations. Once the calculation was completed, the result was sorted to get the chart in an organized and clearly explained manner*. 


**⭐2. Median Salaries By country**

**Key Insights**
- **The United States stands out as a high‑salary benchmark**, consistently positioned among the top‑earning countries in the dataset, reinforcing its role as a global leader in data‑driven and technical job compensation.

- **A strong mid‑tier salary cluster emerges across South Korea, Argentina, Colombia, and Thailand**, each reporting median salaries around $111K–$113K, showing competitive global markets outside the U.S.

- **Europe displays significant salary variation, with countries like Austria, Czech Republic, and Poland** offering salaries above $105K, while others such as Belgium and Greece fall into the $78K–$86K range. Meanwhile, Belarus appears as a major outlier at $400K, suggesting exceptional market conditions.

  The formula used to explore this analysis is given below:
  ```
  =MEDIAN(
  IF((jobs[job_country]=A2)*
  (jobs[salary_year_avg]<>0)*
  (jobs[job_title_short]=title)*
  (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))
  ,jobs[salary_year_avg]))
  ```
![job_country](https://github.com/abdulaikabba19/Data_Science_Jobs_ms_excel/blob/main/images_data_jobs/job_country.png?raw=true)
*This figure shows the result of the data, and the map chart, after the calculation is done.The region marked with blue shows how median salary varied for different countries* 

**⭐3. Job Schedule Type Count**

**Key Insights**
- **Full‑time roles offer the highest median salary**,  which positions them at the top of the job‑type hierarchy and reflects the premium placed on long‑term employment commitments.

- **Contractor, part‑time, and temp roles** form a competitive mid‑tier, showing that flexible or non‑permanent work arrangements can still command strong compensation.

- **Internships sit at the entry point of the salary spectrum**, establishing a clear progression path from early‑career roles through to full‑time positions.
- **The counts of jobs** clearly illustrates that most companies look out for full-time employment, as this help them to create a stable work force.

  The following formula was used to calculate the **job counts** and **job schedule type** respectively:

```
=FILTER(I2#,NOT(ISNUMBER(SEARCH("and",I2#)))*(I2#<>0))
```
```
=MEDIAN(
IF((jobs[job_title_short]=title)*
(jobs[salary_year_avg]<>0)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(A2,jobs[job_schedule_type]))),jobs[salary_year_avg]))
```

  ![job_type](https://github.com/abdulaikabba19/Data_Science_Jobs_ms_excel/blob/main/images_data_jobs/job%20type%20gif.gif?raw=true)
  
*This bar chart is used to show the job counts and job schedule type variations*

## Conclusion
As someone who happens to be a data-driven minded person, this project has helped me to build key skills that are required of me when using MS Excel. Also, as the trends clearly show, it will help me to shape myself to go in for courses that do have high-earning possibilities, and it prepares me to know what are the key skills that are required for these high paying jobs. 



