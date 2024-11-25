# Netflix-and-Prime-Video-Analysis-Dashboard
This Power BI project visualizes data from Netflix and Prime Video, providing insights into various aspects of their content libraries, including film genres, release years, total shows per year, and viewer ratings. The dashboard helps explore patterns and trends in streaming platform content.

# Project Title
# Streaming Service Data Analysis: Netflix vs. Prime Video

## Project Overview
This project focuses on analyzing and comparing data from Netflix and Prime Video to uncover patterns in content offerings, popularity trends, and regional distributions. The workflow involves data cleaning, transformation, and analysis using **Excel** and **SQL**, followed by creating dynamic visualizations in **Power BI**.

---

## Objectives
1. Compare the content catalogs of Netflix and Prime Video by genres, release years, and content ratings.
2. Identify trends in the types of shows/movies popular on each platform.
3. Provide actionable insights to improve content strategies for both streaming platforms.

---

## Process Workflow
### **1. Data Extraction**
- The raw dataset (`netflix_titles (1).csv`) contains information about Netflix and Prime Video content, including titles, genres, ratings, release dates, and regions.
- Tools Used: **Excel**

---

### **2. Data Cleaning and Transformation**
- **Steps in Excel:**
  - Removed duplicate entries for titles available.
  - Cleaned and standardized genre names for consistency.
  - Filled missing values in the `rating` column using logical assumptions (e.g., "TV-MA" for mature content, "G" for general audiences).
  - Created calculated columns for:
    - **Year of Release:** Extracted from release date.
    - **Content Age:** Calculated the age of the content in years.

- **Steps in SQL:**
  - Imported the cleaned dataset into a SQL database.
  - Performed advanced transformations:
    - Filtered content by platform and genre for focused analysis.
    - Created aggregated metrics such as the total number of titles per genre and average rating.
    - Merged datasets for a consolidated comparison.

  Example SQL Query:
  ```sql
  SELECT platform, genre, COUNT(*) AS total_titles, AVG(rating) AS avg_rating
  FROM streaming_data
  GROUP BY platform, genre
  ORDER BY total_titles DESC;
# Data Loading
The cleaned dataset was exported as transformed_streaming_data.csv for integration into Power BI.
Additional calculated metrics and derived fields were included for enhanced analysis.


# Data Visualization
Tool Used: Power BI

Created an interactive dashboard to compare Netflix and Prime Video metrics:

Content Distribution by Genre: Visualized through stacked bar charts.
Average Ratings by Platform: Shown using line and column charts.
Year-Wise Content Additions: Highlighted through a line graph.
Popular Content Regions: Displayed on a map visualization.
Genre Popularity Comparison: Presented via a treemap.


# Power BI Features Utilized:

Dynamic slicers to filter data by platform, genre, and region.
Drill-through capabilities for analyzing specific genres or years.
Custom DAX measures to calculate metrics like average ratings and the number of new releases per year.

# Key Insights
Content Diversity: Netflix offers a wider range of genres, whereas Prime Video focuses more on documentaries and regional content.
Average Ratings: Prime Video's average content rating is slightly higher than Netflix's, indicating better audience reception for its titles.
Release Trends: Netflix consistently releases more content annually, while Prime Video focuses on fewer but higher-rated titles.
Regional Focus: Prime Video has a stronger presence in regional markets compared to Netflix.

# Files in This Repository
- `netflix_titles (1).csv/`: Contains the raw dataset in CSV format.
- `visuals.jpeg/`: Includes JPEG images of visualizations.
- Download the Power BI file: [Netflix Power BI File](Netflix_PowerBI.pbix)

  




# Tools and Technologies
Data Cleaning & Transformation: Microsoft Excel, SQL
Data Visualization: Power BI
Languages: SQL, DAX

# How to Use This Repository
Clone this repository
git clone https://github.com/animax007/Netflix-and-Prime-Video-Analysis-Dashboard.git

# Contact
If you have any questions or want to collaborate, feel free to reach out:

Email: prathamsingh71017@gmail.com
LinkedIn: https://linkedin.com/in/prathamsingh007




