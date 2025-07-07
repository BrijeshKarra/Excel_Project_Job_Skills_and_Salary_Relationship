
# Data Science Jobs - Skills and Salary Relationship

## Introduction
 In this project, I explored how different Data Science job skills affect salary using Power Query, Power Pivot, and DAX in Excel. The project involved cleaning and organizing the data, creating relationships between tables, calculating key metrics, and showing the results through easy-to-understand visuals.




### Questions to Analyze
To get everyone on the same page, the project aims to focus on 4 main questions:

1. **Do more skills get you better pay?**
2. **What’s the salary for data jobs in different regions?**
3. **What are the top skills of data professionals?**
4. **What’s the pay for the top 10 skills?**

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **Pivot Tables**
- **Pivot Charts**
- **DAX (Data Analysis Expressions)**
- **Power Query**
- **Power Pivot**

### Data Jobs Dataset

The [dataset](https://github.com/lukebarousse/Excel_Data_Analytics_Course/tree/main/0_Resources/Datasets) used for this project contains real-world data science job information from 2023, which provides a foundation for analyzing data using Excel.

It includes detailed information on:

- **Job titles**
- **Salaries**
- **Locations**
- **Skills**

## **Investigating The Four Questions:**


## 1. Do more skills get you better pay?

###  Skill: Power Query (ETL)

To see the Power Query implementation [click here](/Skills%20Implemented/Power%20Query/ReadMe.md)

###  Analysis

![Do more skills get you better pay?](/Visuals/Q1_5_plot.png)

####  Insights

Country = Canada
- There is a positive trend between the number of skills and median salary, particularly in roles like Senior Data Scientist and Cloud Engineer.
- Most high-income roles have similar skill counts, with little variation between them, for example, Data Scientist and Senior Data Scientist.

This highlights that having multiple relevant skills helps, but adds limited value at higher-paying levels.



## 2️. What’s the salary for data jobs in different regions?

### Skills: PivotTables & DAX

#### Pivot Table

-  I created a PivotTable using the Data Model I created with Power Pivot.
-  I moved the `job_title_short` to the rows area and `salary_year_avg` into the values area.
-  Then I added new measure to calculate the median salary for Canadian jobs.
    ```
    =CALCULATE(
        MEDIAN(data_jobs_salary[salary_year_avg]),
        data_jobs_salary[job_country] = "Canada")
    ```

####  DAX

- To calculate the median year salary I used DAX.

    ```
    Median Salary := MEDIAN(data_jobs_salary[salary_year_avg])
    ```

###  Analysis

![Q2_1_table](/Visuals/Q2_table.png)


####  Insights

-  Job roles like Senior Data Scientist and Senior Data Engineer command higher median salaries both in Canada and internationally, showcasing the global demand for high-level data expertise.

-  The salary gap between Canadian and non-Canadian roles grows slightly at higher levels, though the variation remains modest


These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.

## 3️. What are the top skills of data professionals?

###  Skill: Power Pivot

To see the Power Pivot implementation [click here](/Skills%20Implemented/Power%20Pivot/ReadMe.md)

### Analysis
![2_Project_Analysis_Chart3.png](/Visuals/Q3_plot.png)
#### Insights

- Python and SQL dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.
- Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

    
Understanding in-demand skills helps professionals stay competitive and helps educators and learning platforms focus on the technologies that matter most in the job market.

## 4️. What’s the pay of the top 10 skills?

###  Skill: Advanced Charts (Pivot Chart)

####  PivotChart

- I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
    -  **Primary Axis:** Median Salary (as a Clustered Column)
    -  **Secondary Axis:** Skill Likelihood (as a Line with Markers)

- To customize the chart, I added an axis title, removed the lines (skill likelihood), and changed the markers to circles.

###  Analysis

![Q4_plot.png](/Visuals/Q4_plot.png)

#### Insights

-  Higher median salaries are associated with skills like Snowflake, Spark, and Azure, suggesting their critical role in high-paying tech jobs.
-  Skills like SQL and Python show the highest skill likelihood, highlighting their widespread use across many applications.

    
This chart highlights the importance of investing time in high-value skills. While tools like Snowflake and Spark are linked to higher salaries, widely used skills like Python and SQL offer greater versatility and help professionals stay competitive.

## Conclusion
In this project, I analyzed job titles, salaries, locations, and key skills using advanced Excel features like Power Query, PivotTables, DAX, and charts. The analysis revealed correlations between multiple skills and higher salaries, regional salary variations, and highlighted essential skills for anyone pursuing a career in data science.

