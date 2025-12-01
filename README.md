# Employee Performance Analysis

## 1.0 Introduction  

This report is an Exploratory Data Analysis (EDA) of a publicly available employee dataset from the FP20 Analytics Data Challenge Group. The aim of the analysis is to demonstrate learned techniques, describe location, variance, and distribution, and explore covariance and correlation within the dataset. This includes uncovering trends in sales, tenure, employee performance, and store analysis. 

### 1.1 Data Description 

The dataset contains 5 sheets:

- **Employees:** Stores information such as demographics, job attributes, salary, managers, hire/exit dates.  
- **Monthly Performance:** Stores training hours, overtime, absenteeism, employee satisfaction, engagement.  
- **Role KPIs:** Stores monthly KPI values measuring productivity.  
- **Stores:** Stores location and store type.  
- **Business Outcomes:** Stores monthly outcomes such as sales, waste %, NPS, delivery timing.

### 1.2 Data Processing Steps 

- Dataset inspected in Excel, then loaded in Python; each sheet imported into a separate DataFrame.  
- Date columns such as `Hire_Date`, `Exit_Date`, and `Opening_Date` converted to datetime format.  
- Missing values were identified and investigated to understand their impact on the analysis.  
- Employee tenure measurements derived from hire and exit dates; new calculated fields added for analysis.  
- Visualizations produced using Matplotlib and Seaborn for readability and clarity.

### 1.3 Methodology

#### 1. Descriptive Statistics (Location & Variability)

- **Measures of Central Tendency (Mean, Median, Mode):** Understand typical employee or store performance values (sales, satisfaction, engagement, tenure, waste %).  
- **Measures of Variability (Standard Deviation & IQR):** Assess how widely data points vary around averages.

#### 2. Distribution Analysis & Visualization

- **Histograms:** Visualize frequency patterns, skewness, clustering, and outliers for Tenure, Waste %, Satisfaction, Delivery Performance.  
- **Boxplots:** Compare spread and detect outliers across categories (employee performance, store metrics).  
- **KDE (Density Curves):** Reveal smooth distribution patterns.

#### 3. Relationship Analysis Between Variables

- **Scatter Plots:** Explore relationships such as:
  - Employee Satisfaction vs Engagement Index  
  - Training Hours vs Performance Rating  
  - Tenure vs Salary / Tenure vs Bonuses  
  - Waste % vs Customer Satisfaction  
- **Correlation Analysis:** Identify strength and direction of relationships between numerical variables.

---

## 2.0 Analysis of The Employee Performance Dataset 

This analysis explores employee performance to identify key patterns and relationships. The objective is to generate actionable insights to support workforce planning and management.

### 2.1 Data Quality Check 

- `df.isnull().sum()` was used to identify duplicates and missing values.  
- Four columns contained missing values: `Exit_Date`, `Manager_Id`, `Manager_Name`, `Manager_Status`.  
- `Exit_Date` had 6009 missing entries, expected since not all employees have exited.

### 2.2 Categorical Summary

- Distribution of categorical variables (department, job level, education level) reviewed to understand workforce composition.

### 2.3 Age Distribution of Employees

- Mean age: 32.5 years  
- Median age: 32 years

### 2.4 Employee Salary Analysis

- Salary histogram shows most employees earn **$20,000–$40,000**, indicating a junior-leaning structure with fewer high-level executives.

### 2.5 Salary by Job Level

- Entry/Associate: $20,000–$40,000  
- Manager/Senior Manager: $60,000–$115,000  
- Executives: up to $175,000  

---

## 3.0 Employee Retention Summary

- **Retention:** 80% still employed, 20% exited  
- **Average tenure:** 5 years, most employees between 4–6 years  
- **Higher salaries associated with longer employment duration**

### 3.1 Employee Distribution and Average Salary by Store Location

| Store_Location | Total_Employees | Average_Salary |
|----------------|----------------|----------------|
| Fort Worth     | 330            | 27,211         |
| Nashville      | 329            | 27,816         |
| San Jose       | 325            | 26,457         |
| Louisville     | 323            | 27,513         |
| Seattle        | 319            | 27,479         |
| Denver         | 316            | 26,863         |
| Los Angeles    | 314            | 27,945         |
| Portland       | 312            | 27,668         |
| Dallas         | 309            | 26,561         |
| Las Vegas      | 306            | 28,090         |
| Philadelphia   | 305            | 26,679         |
| San Antonio    | 303            | 28,121         |
| Phoenix        | 297            | 26,686         |
| Boston         | 297            | 26,849         |
| Detroit        | 294            | 26,265         |
| Charlotte      | 293            | 27,659         |
| Jacksonville   | 293            | 26,775         |
| Baltimore      | 289            | 26,668         |
| Austin         | 285            | 28,139         |
| Houston        | 284            | 27,560         |
| Columbus       | 284            | 27,462         |
| Memphis        | 282            | 27,532         |
| New York       | 279            | 27,796         |
| San Diego      | 270            | 26,594         |
| Chicago        | 262            | 26,878         |

### 3.2 Store Analysis

- Regular stores most common, followed by Superstores; Express stores least prevalent.  
- Store openings rose steadily from 2015, peaked in 2017, declined 2018–2019, and ended with a decline in 2024.

### 3.3 Employee Performance Analysis

- Strong positive relationship between Employee Satisfaction and Engagement Index.  
- Monthly productivity improved YoY, with peaks in the last quarter reaching an index of 2 in Dec 2024.

### 3.4 Sales Analysis

- Most stores achieved close to targets; some overperformed (up to 115%), few underperformed (<85%).  
- Waste percentage mostly 1–5%; few above 5%.  
- On-time delivery rates mostly 92–97%.

---

## Recommendations

1. Review compensation structure: tie salary growth to tenure and performance; benchmark against industry averages.  
2. Establish clear career progression paths and internal mobility programs.  
3. Strengthen performance-linked rewards (bonuses, promotions).  
4. Implement personalized retention strategies, including upskilling and career advancement support.  
5. Expand structured technical, leadership, and certification training; measure impact on career growth.
