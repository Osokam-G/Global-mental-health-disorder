# Global Mental Health Disorder Dashboard

This is a Power BI Project exploring mental health disorder prevalence across countries and over time.

## Table of Contents

1. [Introduction](#1-introduction)
2. [Problem Statement](#2-problem-statement)
3. [Data Sourcing](#3-data-sourcing)
4. [Data Transformation and Cleaning](#4-data-transformation-and-cleaning)
5. [Analytical Measures](#5-analytical-measures)
6. [Dashboard and Visuals](#6-dashboard-and-visuals)
7. [General Insights](#7-general-insights)
8. [Recommendations](#8-recommendation)
9. [Conclusion](#9-conclusion)
10. [Author](#10-author)

## 1. Introduction

This project uses Power BI to explore mental health disorder prevalence across countries and over time. The dashboard summarizes average prevalence measures for depression and anxiety, compares male and female prevalence, and displays country-level and disorder-level patterns.

This analysis reports **231 countries**, **3.50% average depression prevalence**, **3.99% average anxiety prevalence**, **2.80% average male prevalence**, and **4.12% average female prevalence**.

## 2. Problem Statement

Mental health prevalence data can be difficult to compare across countries, disorders, demographic groups, and years. This project brings several views together to help users explore the distribution of reported prevalence and identify patterns that may warrant further investigation.

The analysis focuses on these questions:

- How do the displayed averages differ by gender?
- How does average prevalence vary across mental health disorder categories?
- How does anxiety prevalence vary across countries?
- How has global anxiety prevalence changed over time?

## 3. Data Sourcing

> **Data source:** By Amit. The dataset was provided to me by **Quantum Analytics**, which obtained it from  Amit. I used the dataset for this project’s analysis and dashboard.
- **Dataset name:** `Mental health Depression disorder Data`

## 4. Data Transformation and Cleaning

I used a three-stage workflow to inspect, clean, and validate the dataset before building the Power BI dashboard.

1. **Excel — data inspection:** I checked for missing values, duplicate records, data types, outliers, and extra spacing.
2. **Google Colab — data cleaning:** I cleaned the dataset and addressed the data-quality issues identified during inspection.
3. **Power Query — data validation:** I loaded the cleaned dataset into Power Query and checked its validity and quality to confirm it was suitable for analysis before loading it into Power BI.

### view of the clean dataset in MS EXCEL

<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/bd7fbc7d-d974-40b4-93ea-e3eaf28e6e28" />





## 5. Analytical Measures

### Dax measures

- Average alcohol use disorder
  
  ```AVG alcohol use disorder (%) =
     AVERAGE(merged_table[Alcohol use disorders (%)])
  ```
- Average Anxiety disorder (%)
  
  ```AVG Anxiety disorder =
    DIVIDE(AVERAGE(merged_table[Anxiety disorders (%)]),100)
  ```


- Average Bipolar Disorder
  
```AVG Bipolar Disorder (%) =
  AVERAGE(merged_table[Bipolar disorder (%)])
  ```

- Average depression Prevalence 

```AVG depression Prevalence (%) =
   DIVIDE(AVERAGE(merged_table[Depression (%)]),100)
  ```

- Average drug use disorder
  
```AVG drug use disorder =
  AVERAGE(merged_table[Drug use disorders (%)])
  ```

- Average Eating Disorders

```AVG Eating Disorders =
  AVERAGE(merged_table[Eating disorders (%)])
  ```

- AVG female prevalence
 
 ```AVG female prevalence =
  DIVIDE(AVERAGE(merged_table[Prevalence in females (%)]),100)
```


- Average male prevalence 

 ```AVG male prevalence =
   DIVIDE(AVERAGE(merged_table[Prevalence in males (%)]),100)
```



- Average Schizophrenia
  
 ```AVG Schizophrenia % =
  AVERAGE(merged_table[Schizophrenia (%)])
```



- Number of countries covered
 
 ```Number of countries covered =
    DISTINCTCOUNT(merged_table[Entity])
```



- Overall Mental Health Prevalence
 
 ``Overall Mental Health Prevalence = 
DIVIDE(
    [AVG Schizophrenia %] +
    [AVG Bipolar Disorder (%)] +
    [AVG Eating Disorders (%)] +
    [AVG Anxiety disorder] +
    [AVG alcohol use disorder (%)] +
    [AVG depression Prevalence] +
    [AVG drug use disorder (%)],
    7)
    ```


The dashboard displays the following summary measures:

| Measure | Dashboard value |
|---|---:|
| Number of countries | 231 |
| Average depression prevalence | 3.50% |
| Average anxiety disorder prevalence | 3.99% |
| Average male prevalence | 2.80% |
| Average female prevalence | 4.12% |



## 6. Dashboard and Visuals

The dashboard contains:

- KPI cards for country count and average depression, anxiety, male, and female prevalence.

- A horizontal bar chart of mental health disorder prevalence by country.

<img width="1920" height="1080" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/1a540485-2c8c-4371-bacb-7923a0b87ec9" />



- A horizontal bar chart comparing average prevalence across disorder categories.

<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/0a4cbf47-221d-4cfc-a512-b224a5939d1f" />



- A column chart showing anxiety disorder prevalence by country.

<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/0725c1f0-ad4d-472d-b76b-e90bd84d0220" />



- A line chart showing global anxiety disorder prevalence over time.

<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/29705afa-e078-4fd2-a4b1-1b95d39862b8" />



- A country slicer for interactive filtering.


<img width="1920" height="1080" alt="Screenshot (82)" src="https://github.com/user-attachments/assets/97266e65-0c15-4154-bbfc-d58b6e738827" />


## 7. General Insights

- The Analysis covers **231 countries**.
- The displayed average anxiety prevalence is **3.99%**, compared with **3.50%** for depression.
- The displayed average female prevalence is **4.12%**, compared with **2.80%** for males. 
- In the disorder comparison chart, Alcohol Use Disorders has the longest bar, followed by Drug Use Disorders and Bipolar Disorder. 
- The time-series chart shows global anxiety prevalence increasing from the early 1990s to around 2010, then remaining relatively steady with a small decline near the end of the displayed period.

## 8. Recommendation

- **Prioritize prevention and support for anxiety and depression.** Their displayed average prevalence is 3.99% and 3.50%, respectively. Use these figures to guide further investigation and planning.
- **Investigate the gender difference in the dashboard.** The displayed averages are 4.12% for females and 2.80% for males. Examine whether this pattern is consistent across countries and years.
- **Study the anxiety trend over time.** The chart shows an increase from the early 1990s to around 2010, followed by a relatively steady level. Investigate this pattern alongside changes in data coverage and measurement before using it to guide policy.


## 9. Conclusion

This Power BI project presents a high-level view of mental health disorder prevalence across countries and years. The dashboard reports average depression prevalence of 3.50% and average anxiety prevalence of 3.99%, alongside comparisons by gender, disorder category, country, and year. The visuals can help users explore broad patterns, while interpretation depends on documenting the data source, coverage, measure definitions, and cleaning steps.

## 10. Author

**OSOKAM GIFT**

- [LinkedIn](https://www.linkedin.com/in/osokam-gift-375124291?utm_source=share_via&utm_content=profile&utm_medium=member_android)
- [Portfolio](add-your-link)
- [GitHub](add-your-link)
