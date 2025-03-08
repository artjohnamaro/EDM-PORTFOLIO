# Midterm Lab Task 2 – Data Cleaning and Transformation Using Power Query Editor

## Task Description:
This task involves cleaning, transforming, and analyzing a dataset of job listings using Power Query in Excel. The process is structured to ensure the data is accurate, organized, and ready for meaningful insights.

## Dataset before doing Cleaning and Transformation
![Image Alt](https://github.com/artjohnamaro/EDM-PORTFOLIO/blob/8aedfc1b34f5ead8dc776bf729e2c452c8b74517/images/481862011_1667588200824136_8244213805779384497_n.png)

## Steps perform in Data Cleaning and Transformation

**1. Load Data into Excel**

- Go to Data → New Query → Open File → Select CSV → Load and Edit in Power Query Editor.

**2. Data Cleaning Steps**

- Duplicate Raw Data for backup.
  
- Salary Estimate Column: Extract text before (.
  
- Min Sal & Max Sal Columns: Use Column from Examples to extract salary ranges.
  
- Role Type Column: Create a custom column with conditions for common job roles.
  
- Location Correction Column: Add custom logic to standardize locations and split by , delimiter.
  
- Handle Outliers: Filter and correct values in relevant columns like competitors, revenues, and industry.
  
- Company Name Cleaning: Remove extra text (like ratings) from company names.
  
- Remove Descriptions Column for clarity.
  
**3. Data Transformation and Grouping**

Duplicate Data for Salary Analysis:

- Select Role Type, Min Sal, and Max Sal.
  
- Convert salaries to currency and multiply by 1000.
  
- Group by Role Type and calculate average salaries.
  
Reference Data for Salary by Company Size:

- Select Size, Min Sal, and Max Sal.
  
- Convert salaries to currency and multiply by 1000.
  
- Group by Size and calculate average salaries.
  
**4. Mapping State Data**

- Import State Mapping workbook.
  
- Merge state abbreviations with full names.
  
- Filter out null or blank values.

**5. Reference Data for Salary by State**

- Select State Full Name, Min Sal, and Max Sal.
  
- Convert salaries to currency and multiply by 1000.
  
- Group by State Full Name and calculate average salaries.

## Final Output
![Image Alt](https://github.com/artjohnamaro/EDM-PORTFOLIO/blob/3f797e6b5a815796adca1111d614062ba35f8e03/images/Cleaned_Data.PNG)
![Image Alt](https://github.com/artjohnamaro/EDM-PORTFOLIO/blob/e8b9fc6818664a2d0e60151d9b344b4f94f6f1d9/images/Data%20Query%20Structure.PNG)
