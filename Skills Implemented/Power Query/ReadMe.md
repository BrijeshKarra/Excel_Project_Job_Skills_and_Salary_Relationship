# Power Query Implementation


##  Extract

- I first used Power Query to extract the original data (`data_salary_all.xlsx`) and create two queries:

    - First one, `data_jobs_salary` with all the data jobs information.
    -  The second, `data_jobs_skills`, listing the skills for each job ID.

## Transform

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

    -  data_jobs_salary

        ![Q1_1_salary.png](/Visuals/Q1_1_salary.png)


    - data_job_skills


        ![Q1_2_skills.png](/Visuals/Q1_2_skills.png)

## Load

- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.

    -  data_jobs_salary

        ![Q1_3_salary.png](/Visuals/Q1_3_salary.png)

    -  data_job_skills

        ![Q1_4_skills.png](/Visuals/Q1_4_skills.png)
