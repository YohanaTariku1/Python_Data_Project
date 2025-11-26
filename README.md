# The Analysis

## 1. What are the  most demanded skills for the top 3 most popular data roles?

To identify the most in-demand skills for the three most common data roles, I first determined which job titles appeared the most frequently. Then, for each of those roles, I pulled out the top five required skills. This gives a clear picture of which skills are most valuable for each role and helps me understand what to focus on depending on the career path I want to pursue.

View my notebook with detailed steps here: [2_Skill_Demand.ipynb](2_Project\2_Skill_Demand.ipynb)

### Visualize Date

```python
fig, ax = plt.subplots(len(job_titles), 1)

for i, job_title in enumerate(job_titles):
    df_plot = df_skills_perc[df_skills_perc['job_title_short'] == job_title].head(5)
    sns.barplot(data=df_plot, x='skill_percent', y='job_skills', ax=ax[i], hue='skill_percent', palette='dark:b_r', legend=False)

plt.show()
```

### Results

![Visualization of Top Skills for Data Roles](2_Project\images\skill_demand_by_role.png)

### Insights

- SQL remains the core skill for Data Analysts and Data Scientists, appearing in more than half of all job postings for both roles.

- Python is the top requirement for Data Engineers (68%) and is also highly demanded for Data Scientists (72%), showing its importance in more technical and modeling-focused roles.

- Data Engineers are expected to work with cloud and big-data technologies such as AWS, Azure, and Spark — tools not typically required for Data Analysts.

- Data Analysts rely more on business-focused tools like Excel and Tableau, reflecting their emphasis on data reporting and visualization.

- Across all roles, Python and SQL form the core skill set, while specialization depends on the role’s focus — engineering, analysis, or advanced modeling.
