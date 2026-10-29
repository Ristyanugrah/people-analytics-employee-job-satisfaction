# People Analytics: Employee Job Satisfaction Analysis

## Project Overview

This project analyzes employee survey data to identify factors associated with job satisfaction. Using Python, exploratory data analysis (EDA), correlation analysis, and statistical hypothesis testing, the project examines the relationships between job satisfaction and workplace factors such as workload, work-life balance, work environment, stress, sleep duration, and overtime.

The objective is to generate actionable insights and data-driven recommendations that can support Human Resources (HR) decision-making and employee well-being initiatives.

## Business Objectives

- Analyze the overall distribution of employee job satisfaction.
- Identify workplace and well-being factors associated with job satisfaction.
- Compare satisfaction levels across departments, job levels, and overtime status.
- Validate observed relationships using statistical methods.
- Develop practical recommendations to improve employee experience and workplace conditions.

## Dataset Overview

The dataset contains **2,766 employee records and 23 columns**.

| Category | Key Variables |
|---|---|
| Demographics | Gender, age, marital status, education level |
| Employment | Job level, experience, department, employment type |
| Workplace factors | Work-life balance, work environment, workload, stress |
| Well-being | Sleep hours, physical activity hours |
| Work arrangements | Overtime status, commute mode, commute distance |
| Organizational factors | Number of companies, team size, number of reports, annual training hours |
| Target variable | Job satisfaction |

The `job_satisfaction` variable is measured on a scale from 1 to 5.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Google Colab

## Project Workflow

### 1. Data Understanding

- Inspected dataset dimensions, column names, data types, and descriptive statistics.
- Identified employee characteristics and workplace variables relevant to job satisfaction.

### 2. Data Cleaning and Validation

- Checked missing values and duplicate records.
- Reviewed categorical distributions and numerical ranges.
- Performed logical validation on age, experience, sleep hours, and commute distance.
- Identified potential outliers using the Interquartile Range (IQR) method.

**Data quality summary:**
- Total records: 2,766
- Total columns: 23
- Missing values: None detected
- Exact duplicate rows: None detected
- Potential outliers: 6 in physical activity hours and 13 in sleep hours

Potential outliers were identified for further review and were not automatically removed.

### 3. Exploratory Data Analysis (EDA)

Explored job satisfaction patterns across:

- Work-life balance scores
- Work environment scores
- Workload levels
- Stress levels
- Overtime status
- Departments and job levels
- Sleep duration and work experience

### 4. Correlation Analysis

Used Pearson correlation for an initial examination of numerical relationships and Spearman rank correlation to assess monotonic associations between selected factors and job satisfaction.

### 5. Statistical Validation

- **Spearman correlation:** Examined associations between workplace factors and job satisfaction.
- **Welch's independent-samples t-test:** Compared average satisfaction between employees with and without overtime.
- **One-way ANOVA:** Evaluated differences in average satisfaction across departments and job levels.

### 6. Data Visualization

Created charts and a correlation heatmap to communicate satisfaction distributions, workplace patterns, and relationships between selected variables.

## Key Findings

### 1. Overall Job Satisfaction

The average job satisfaction score was **3.38 out of 5**.

| Satisfaction Score | Number of Employees | Percentage |
|---:|---:|---:|
| 1 | 388 | 14.0% |
| 2 | 254 | 9.2% |
| 3 | 519 | 18.8% |
| 4 | 1,127 | 40.7% |
| 5 | 478 | 17.3% |

A score of 4 was the most common response, accounting for 40.7% of employees.

### 2. Factors Associated with Job Satisfaction

The notebook's final factor summary reports the following Spearman correlation coefficients:

| Factor | Spearman Correlation | Direction |
|---|---:|---|
| Workload | -0.252 | Negative |
| Work-Life Balance | +0.247 | Positive |
| Work Environment | +0.246 | Positive |
| Stress | -0.191 | Negative |
| Sleep Hours | +0.169 | Positive |

The results suggest that higher workload and stress are associated with lower job satisfaction, while better work-life balance, a better work environment, and longer sleep duration are associated with higher satisfaction.

These associations do not establish causation.

### 3. Overtime Analysis

Employees without overtime had an average satisfaction score of **3.51**, compared with **3.09** for employees with overtime.

- Mean difference: 0.42 points
- Welch's t-statistic: 7.893
- P-value: approximately 5.57 × 10⁻¹⁵

The difference was statistically significant at the 5% significance level.

### 4. Department and Job-Level Analysis

The one-way ANOVA results did not find statistically significant differences in average job satisfaction across departments or job levels at the 5% significance level.

| Analysis | F-statistic | P-value |
|---|---:|---:|
| Department | 1.162 | 0.321 |
| Job Level | 0.433 | 0.785 |

These results do not prove that all groups have identical satisfaction levels. They indicate that the analysis did not find sufficient statistical evidence of differences in group means.

## Business Recommendations

### 1. Review Workload and Overtime

Monitor overtime frequency and workload distribution. Review staffing capacity and work allocation to identify teams that may need additional support.

### 2. Improve Work-Life Balance

Encourage reasonable workloads, effective time management, and flexible working arrangements where operationally feasible.

### 3. Strengthen the Work Environment

Collect employee feedback on workplace conditions, collaboration, management support, and access to necessary resources.

### 4. Support Stress Management

Introduce employee check-ins and appropriate well-being initiatives. Investigate organizational contributors to stress rather than focusing solely on individual coping strategies.

### 5. Monitor Employee Well-Being

Track job satisfaction and related workplace indicators through recurring employee surveys to evaluate changes over time.

### 6. Apply Data-Driven HR Decisions

Develop an HR reporting dashboard to monitor satisfaction levels, overtime patterns, and workplace indicators across employee groups.

## Limitations

- The analysis identifies associations rather than causal relationships.
- The dataset's sampling method and representativeness are not established in the notebook.
- Statistical significance does not necessarily imply practical significance.
- Potential outliers require further investigation to determine their impact on results.
- The analysis does not establish whether the observed patterns persist over time.
- The reported factor correlations should be checked against the actual Spearman analysis output before being used for formal reporting.

## Repository Structure

```text
people-analytics-employee-job-satisfaction/
├── people_analytics_employee_job_satisfaction.ipynb
└── README.md
```

## How to Run

1. Clone or download this repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Install the required Python libraries if necessary.
4. Ensure the employee survey dataset is available at the file path specified in the notebook.
5. Run the notebook cells sequentially.

## Author

**Risty Anugrah Dwi Septiana**

- GitHub: [Ristyanugrah](https://github.com/Ristyanugrah)
- Data Analytics Portfolio: [GitHub Repository](https://github.com/Ristyanugrah/data-analytics-portfolio)
- Website: [Personal Portfolio](https://risty-portfolio.vercel.app/)

## Conclusion

This project demonstrates how exploratory data analysis and statistical testing can help identify workplace factors associated with employee job satisfaction. The findings highlight workload, work-life balance, work environment, stress, and overtime as important areas for further investigation and evidence-based HR initiatives.
