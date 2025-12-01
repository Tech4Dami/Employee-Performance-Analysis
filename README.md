 
1.0 Introduction  

This report is an Exploratory Data Analysis (EDA) of a publicly available employee dataset from the FP20 Analytics Data Challenge Group. The aim of the analysis is to demonstrate learned techniques, to describe location, variance, and distribution, and to explore the covariance and correlation within the dataset. This includes uncovering trends in sales, tenure, employee performance, and store analysis. 

1.1 Data Description 

The dataset countains 5 sheets namely;

Employees: Stored information such as demographics, job attributes, salary, managers, hire/exit dates.
 
Monthly Performance: Stored information such as training hours, overtime, absenteeism, employee satisfaction, engagement.
 
Role KPIs: Stored information such as monthly KPI values measuring productivity.
 
Stores: It stored the location and store type.
 
Business Outcomes: Stored-level monthly outcomes such as sales, waste %, NPS, delivery timing.
 
1.2 Data Processing Steps 

•	The dataset was first inspected on Excel, then loaded from excel using python, and each sheet was imported into a separate Dataframe.
•	Date columns such as Hire_Date, Exit_Date, and Opening_Date were converted to datetime format. 
•	Missing values were identified, and columns with nulls investigated to understand the impact on the analysis.
•	Employee Tenure measurements were derived using hire and exit dates, and new calculated fields were added for analysis.
•	Visualizations were produced using Matplotlib and Seaborn following best practices for readability and clarity.
1.3 Methodology

1.	Descriptive Statistics (Location & Variability):
These methods were used to understand the basic structure and spread of the dataset:

•	Measures of Central Tendency (Mean, Median, Mode): Used to understand typical employee or store performance values such as sales, satisfaction, engagement, tenure, waste percentage, etc.

•	Measures of Variability (Standard Deviation & IQR): Applied to assess how widely data points like performance ratings, bonus amounts, tenure duration, and waste percentages vary around their averages.

2.	Distribution Analysis & Visualization:
 Visual methods were used to show how variables are distributed across employees and stores: 
•	Histograms: Used for variables like Tenure, Waste Percentage, Satisfaction Scores, and Delivery Performance to visualize frequency patterns, skewness, clustering, and outliers. 
•	Boxplots: Used to compare the spread and detect outliers across categories—e.g., employee performance measures, store metrics. 
•	KDE (Density Curves): Applied in some histograms to reveal smooth distribution patterns.

3.	Relationship Analysis Between Variables:
To understand how variables influenced one another, techniques included:
•	Scatter Plots: Used for relationships such as:
•	Employee Satisfaction vs Engagement Index
•	Training Hours vs Performance Rating
•	Tenure vs Salary / Tenure vs Bonuses
•	Waste Percentage vs Customer Satisfaction
•	Correlation Analysis: Used to identify the strength and direction of relationships between numerical variables. This helped highlight which HR or business outcome metrics move together or have meaningful connections.
2.0 Analysis of The Employee Performance Dataset 

This analysis explores employee performance to identify key patterns and relationships within the workforce. The objective is to generate actionable insights that can support better workforce planning and management such as understanding how factors like education, age, and job level influence salary levels and tenure.
2.1 Data Quality Check 

The " df.isnull().sum()" code was used to identify duplicate entries and missing values across all columns. The results showed that four columns contained missing values: "Exit_Date," "Manager_Id," "Manager_Name," and "Manager_Status." Specifically, "Exit_Date" had a large number of missing entries (6009), which was expected because not all employees had left the organization.
2.2 Categorical Summary

I reviewed the distribution of categorical variables such as department, job level, and education level. This helped me understand the composition of the workforce.
  

 
 
2.3 Age Distribution of Employee

I visualized the age distribution of the workforce to understand its population structure. The mean age is 32.5 years, and the median age is 32.0 years.
 
2.4 Employee Salary Analysis

To understand compensation patterns, employee annual salaries were plotted using a distribution graph. The histogram revealed that salaries were heavily concentrated between 20,000and40,000, indicating that the company workforce primarily consists of early career and associate level employees. This suggests a junior-leaning organizational structure with fewer high-level executive roles.
 

2.5 Salary By Job Level

The salary distribution shows an upward progression from entry-level through Executive roles. Entry and Associate staff mostly earn between 20,000 & 40,000 USD, while Manager and Senior Manager level staff earn between 60,000 & 115,000 USD. Executive salaries earn as high as 175,000 USD per annum.
 
3.0 Employee Retention Summary

The analysis shows that 80% of the workforce still work in the company, while 20% have exited. This indicates a strong retention rate, suggesting that the organization has been able to maintain a stable workforce over the observed period.
 
The workforce has an average tenure of 5 years, with most employees working between 4 and 6 years. A small percentage of the workforce has been with the company for 10 years or more, which suggests the company may rely on early-career talent with opportunities for internal development.     
Majority of employees who earned between 10,000 & 30,000 USD worked for 1–4 years, whereas those who earned above 40,000 USD typically stayed for more than 4 years, indicating that higher salaries were generally associated with longer employment duration.
 
3.1	Employee Distribution and Average Salary by Store Location

The table below shows that most stores have a workforce of 310 to 330 employees with an average salary of 27,000 USD indicating consistency in staffing and pay across the companies stores.
|    | Store_Location   |   Total_Employees |   Average_Salary |
+====+==================+===================+==================+
|  0 | Fort Worth       |               330 |            27211 |
+----+------------------+-------------------+------------------+
|  1 | Nashville        |               329 |            27816 |
+----+------------------+-------------------+------------------+
|  2 | San Jose         |               325 |            26457 |
+----+------------------+-------------------+------------------+
|  3 | Louisville       |               323 |            27513 |
+----+------------------+-------------------+------------------+
|  4 | Seattle          |               319 |            27479 |
+----+------------------+-------------------+------------------+
|  5 | Denver           |               316 |            26863 |
+----+------------------+-------------------+------------------+
|  6 | Los Angeles      |               314 |            27945 |
+----+------------------+-------------------+------------------+
|  7 | Portland         |               312 |            27668 |
+----+------------------+-------------------+------------------+
|  8 | Dallas           |               309 |            26561 |
+----+------------------+-------------------+------------------+
|  9 | Las Vegas        |               306 |            28090 |
+----+------------------+-------------------+------------------+
| 10 | Philadelphia     |               305 |            26679 |
+----+------------------+-------------------+------------------+
| 11 | San Antonio      |               303 |            28121 |
+----+------------------+-------------------+------------------+
| 12 | Phoenix          |               297 |            26686 |
+----+------------------+-------------------+------------------+
| 13 | Boston           |               297 |            26849 |
+----+------------------+-------------------+------------------+
| 14 | Detroit          |               294 |            26265 |
+----+------------------+-------------------+------------------+
| 15 | Charlotte        |               293 |            27659 |
+----+------------------+-------------------+------------------+
| 16 | Jacksonville     |               293 |            26775 |
+----+------------------+-------------------+------------------+
| 17 | Baltimore        |               289 |            26668 |
+----+------------------+-------------------+------------------+
| 18 | Austin           |               285 |            28139 |
+----+------------------+-------------------+------------------+
| 19 | Houston          |               284 |            27560 |
+----+------------------+-------------------+------------------+
| 20 | Columbus         |               284 |            27462 |
+----+------------------+-------------------+------------------+
| 21 | Memphis          |               282 |            27532 |
+----+------------------+-------------------+------------------+
| 22 | New York         |               279 |            27796 |
+----+------------------+-------------------+------------------+
| 23 | San Diego        |               270 |            26594 |
+----+------------------+-------------------+------------------+
| 24 | Chicago          |               262 |            26878 |
+----+------------------+-------------------+------------------+
3.2 Store Analysis
The chart below shows that Regular stores are the most common, followed by Superstores, with Express stores being the least prevalent.
This suggests a primary focus on standard retail outlets, with limited smaller-format locations.
 
Store openings rose steadily from 2015, reaching a peak in 2017 before declining in 2018–2019. Activity picked up again after 2020 but remained volatile, ultimately ending with a significant decline in 2024.
 
3.3 Employee Performance Analysis
The scatter plot below illustrated a strong positive relationship between Employee Satisfaction and Engagement Index. As satisfaction increased, engagement levels consistently rose. Suggesting that employees who reported higher satisfaction were generally more engaged in their roles.
 
Employee monthly productivity improved over YoY, with minor mid-year dips. Peaks are observed in the last quarter of each year, reaching a index of 2 in December 2024.
 
3.4 Sales Analysis
Analysis of store sales performance shows most stores achieved close to their targets, with average performance slightly above 100%. Several stores significantly over-performed, reaching up to 115%, while a few under-performed, dipping below 85%.
 
The distribution of waste percentage showed a wide spread, with most stores reporting waste levels between 1% and 5%, with only a small number of stores experienced waste levels above 5%
 
The distribution shows that most stores consistently achieve high on time delivery rates, with the majority of values clustering between 92% and 97%
 
Recommendations
1.	The organization should review its compensation structure by introducing structured salary growth tied directly to employee tenure and performance. Additionally, conducting regular salary benchmarking against industry averages will ensure that the company remains competitive.
2.	Clear career progression paths should also be established. This includes defining transparent promotion criteria and creating internal mobility programs that allow employees to access growth opportunities and move into higher-level roles within the organization.
3.	Performance-linked rewards should be strengthened so that bonuses, salary increases, and promotions are visibly connected to employee KPIs, engagement scores, and demonstrated performance outcomes. This will help reinforce a merit-based culture.
4.	To prevent salary-driven attrition, the company should implement personalized retention strategies such as targeted upskilling programs, career advancement support, and professional development training for employees showing strong potential.
5.	Lastly, employee development initiatives should be expanded to include structured technical, leadership, and certification training. The impact of these programs should be measured consistently to ensure they contribute meaningfully to career advancement and long-term salary growth.

