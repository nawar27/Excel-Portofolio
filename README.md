# Excel Salary Dashboard
 
![gif](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/1.gif)

## Introduction

This Excel Salary Dashboard is designed to help job seekers easily understand various job roles along with their corresponding salary ranges. With a concise and interactive layout, the dashboard allows users to explore salary information based on positions and job categories, making it a practical guide for career planning or salary negotiations.

The dashboard is built using Microsoft Excel, utilizing features such as PivotTables, slicers, and interactive charts. The data includes information on location, main job roles, and the levels or positions within each role. This combination of data helps users gain a more comprehensive and relevant view of salary trends across different regions and position levels.


My final dashboard can access here : [Salary dashboard](https://github.com/nawar27/Excel-Portofolio/blob/main/data_science_salaries_dashboard.xlsx)

### Excel Skills Used

Skills required for data analysis using Excel include :
- 📉 **Charts**
- 🧮 **Formulas and Function**
- ❎ **Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2020 - 2023. The dataset is from [Kaggle](https://www.kaggle.com/datasets/hummaamqaasim/jobs-in-data). It includes detailed information on :
- 👨‍💼 Job titles
- 💰 Salary
- 📍 Residence
- 🎚️ Experience Level

## Dashboard Build

### 📉Charts
📊 **Data Science Job Salaries - Bar Chart**
![bar chart](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/2.png)

- 🛠️ Excel Tools Used: Employed Excel’s map chart functionality to visualize median salaries by country.

- 🎨 Visualization Approach: Applied color gradients to distinguish salary ranges across various regions.

- 📊 Data Display: Displayed median salary figures for countries where data was available.

- 👁️ Visual Enhancement: Enhanced visual clarity to allow for quicker interpretation of salary distribution by geography.

- 💡 Insights Gained: Provided an at-a-glance view of global income variations, emphasizing regions with the highest and lowest median salaries.

## 🧮 Formulas and Functions

 **💰 Median Salary by Country**

 ```excel
=MEDIAN(
      IF(
         (jobs[employee_residence]=A2)*
         (jobs[salary_in_usd]<>0)*
         (jobs[job_title]=title)*
         (jobs[experience_level]=level);
         jobs[salary_in_usd]
      )
)
 ```

 - 🔍 **Multi-Criteria Filtering**: Checks job title, country, employement type, and excludes blank salaries.

- 📊 **Array Formula**: Utilizes MEDIAN() function with nested ``IF()`` statement to analyze an array.

- 🎯 **Tailored Insights**: Provides specific salary information for job titles, country, and employement types.

- 🔢 **Formula Purpose**: This formula populates the table below, returning the median salary based on job title, country, and type specified.

📋 **Background Table**
![table](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/3.png)

📉 **Dashboard Implementation**
![pic](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/4.png)

⏰ **Count of Job Schedule Type**

```excel
=XLOOKUP(title;D2:D126;E2:E126;"No Result")
```

- 🔍 Unique List Generation: This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.

- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of employement types.

**Background Table**

![image](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/5.png)

**Dashboard Implementation**

![image](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/6.png)


## ❎ Data Validation

### 🔍 Filtered List

- 🔒 **Enhanced Data Validation**: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:

  - 🎯 User input is restricted to predefined, validated schedule types

  - 🚫 Entry errors and inconsistencies are effectively avoided
  - 👥 The dashboard’s overall user experience is significantly improved

  ![gif](https://github.com/nawar27/Excel-Portofolio/blob/main/Images/7.gif)

## Conclusion

I developed this dashboard to present insights into salary trends across different data-related job roles. Based on data from my Excel course, it enables users to make informed career decisions by exploring how factors like location and job type impact salaries.
