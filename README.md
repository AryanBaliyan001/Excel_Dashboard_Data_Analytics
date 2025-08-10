# **Excel_Dashboard_Data_Analytics**
![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/a016eddf-83ec-46e7-b4cf-e7beddd18caa)
## **Introduction**
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### **Dashboard File**

My final dashboard is in [Salary_Dashboard.xlsx](Salary_Dashboard.xlsx)

### **Excel Skills Used**

The following Excel skills were utilized for analysis:

-  **📉 Charts**

-  **🧮 Formulas and Functions**

-  **❎ Data Validation**

### **Data Jobs Dataset**

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

-  **👨‍💼 Job titles**
-  **💰 Salaries**
-  **📍 Locations**
-  **🛠️ Skills**

## **Dashboard Build**
### **📉 Charts**

**📊 Data Science Job Salaries - Bar Chart**

<img width="1336" height="867" alt="image" src="https://github.com/user-attachments/assets/7dfafa8c-6202-41e4-bd60-10bd549a0830" />

-  **🛠️ Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.

-  **🎨 Design Choice:** Horizontal bar chart for visual comparison of median salaries.

-  **📉 Data Organization:** Sorted job titles by descending salary for improved readability.

-  **💡 Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

**🗺️ Country Median Salaries - Map Chart**

![Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/e0d1cfa2-9393-4c6e-99ce-a9b51f7d622e)


-  **🛠️ Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.

-  **🎨 Design Choice:** Color-coded map to visually differentiate salary levels across regions.

-  **📊 Data Representation:** Plotted median salary for each country with available data.

-  **👁️ Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.

-  **💡 Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### **🧮 Formulas and Functions**

**💰 Median Salary by Job Titles**

    =MEDIAN(
      IF(
      (jobs[job_title_short]=A2)*
      (jobs[job_country]=country)*
      (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
      (jobs[salary_year_avg]<>0),
      jobs[salary_year_avg]
      )
    )

-  **🔍 Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
-  
-  **📊 Array Formula:** Utilizes MEDIAN() function with nested IF() statement to analyze an array.
-  
-  **🎯 Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
-  
-  **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

**🍽️ Background Table**

<img width="265" height="220" alt="image" src="https://github.com/user-attachments/assets/d83a5245-e463-4e2a-9b2e-310175434db5" />

**📉 Dashboard Implementation**

<img width="1148" height="1214" alt="image" src="https://github.com/user-attachments/assets/1bd952cc-d6ed-4060-90b8-6b2adf590c1c" />

**⏰ Count of Job Schedule Type**

    =FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

-  **🔍 Unique List Generation:** This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.

-  **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

**🍽️ Background Table**

<img width="195" height="119" alt="image" src="https://github.com/user-attachments/assets/cacc7eaf-77b8-46bd-a655-7b9e324c6a62" />

**📉 Dashboard Implementation:**

<img width="942" height="1212" alt="image" src="https://github.com/user-attachments/assets/5a3976ef-a2fb-4df9-8604-763889512ce3" />

## **❎ Data Validation**

**🔍 Filtered List**

-  **🔒 Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
 
    -   🎯 User input is restricted to predefined, validated schedule types

    -   🚫 Incorrect or inconsistent entries are prevented

    -   👥 Overall usability of the dashboard is enhanced
 
![Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/f210623c-2a06-42d3-b7fb-6aac0b9639ba)


## **Conclusion**

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.







