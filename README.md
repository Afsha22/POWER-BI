# Netflix Dashboard - Power BI Project

This project leverages Power BI to perform an end-to-end analysis of Netflix content. Using advanced data modeling, transformation, and visualization techniques, this dashboard provides actionable insights into content ratings, genres, duration, and geographic distribution.

## Objective

The goal of this project is to extract meaningful patterns from the Netflix dataset and present them through an interactive dashboard. This analysis helps:

* Understand audience targeting through ratings and genres
* Identify dominant content categories and regional presence
* Track contributions from top directors and popular content types
* Support business decisions regarding content strategy and localization

 # Dataset link: https://github.com/Afsha22/POWER-BI/blob/main/netflix_titles.csv


## Dataset Description

The dataset consists of content streamed on Netflix, with the following attributes:

| Column Name      | Description                                                 |
| ---------------- | ----------------------------------------------------------- |
| `show_id`        | Unique identifier for each title                            |
| `title`          | Name of the movie or show                                   |
| `type`           | Movie or TV Show                                            |
| `director`       | Director of the content                                     |
| `cast`           | Leading actors in the content                               |
| `country`        | Country of production                                       |
| `date_added`     | Date when the content was added to Netflix                  |
| `release_year`   | Year of release                                             |
| `rating`         | Content rating (e.g., TV-MA, PG-13)                         |
| `duration`       | Runtime in minutes (movies) or number of seasons (TV shows) |
| `listed_in`      | Genre/category of the content                               |
| `description`    | Summary or synopsis of the content                          |
| `murder_mystery` | Custom column added to identify murder mystery content      |
| `first_category` | First genre label extracted from the listed genres          |

## Tools & Technologies

| Tool                                | Purpose                                |
| ----------------------------------- | -------------------------------------- |
| **Power BI Desktop**                | Dashboard design and interactivity     |
| **Power Query**                     | Data cleaning and transformation (ETL) |
| **DAX (Data Analysis Expressions)** | Calculated columns and measures        |
| **Data Modeling**                   | Defining relationships and star schema |

##  Data Cleaning & Preparation Steps

1. **Loading Data into Power BI:**

   * Imported CSV file containing Netflix content.
   * Ensured correct data types for each column (e.g., `date_added` as Date, `duration` as Whole Number or Text).

2. **Power Query Transformations:**

   * Removed null or duplicate values in critical fields.
   * Split the `duration` column into numeric values for analysis.
   * Created a new **custom column**: `Murder Mystery?` by checking if the title or description contains relevant keywords.
   * Extracted the **first genre** from the `listed_in` column for simplified genre analysis.

3. **Calculated Columns and Measures (DAX):**

   * `Total Duration (mins)` – to sum content runtime.
   * `Content by Rating`, `Content by Country`, etc. – measures for interactivity.
   * Slicers and filters for `Type`, `Year`, `Genre`, and `Rating`.

## Dashboard Overview

The dashboard consists of **6 key visualizations**, each offering deep insights:

### 1. Sum of Duration by "Murder Mystery?"

* **Purpose:** Shows total watch time of murder mystery content vs. others.
* **Insight:** Only \~9% of the total duration belongs to murder mystery content.

### 2. Sum of Release Year by Rating

* **Purpose:** Evaluates the trend of content added over years for each rating.
* **Insight:** TV-MA and TV-14 dominate Netflix’s release history, suggesting a focus on mature audiences.

### 3. Country-wise Content by Type

* **Purpose:** Compares the number of movies and shows produced across countries.
* **Insight:** Movies are more globally distributed than TV shows.

### 4. Count of Shows by First Genre

* **Purpose:** Identifies the most frequent first-listed genre.
* **Insight:** Children & Family genre is highly represented in the selected dataset.

### 5. Murder Mystery Content by Rating

* **Purpose:** Analyzes the rating distribution of murder mystery titles.
* **Insight:** Most are rated TV-MA or TV-14, aligning with crime/thriller genre expectations.

### 6. Rating Distribution by Director

* **Purpose:** Shows directors contributing to rated content volume.
* **Insight:** One or two directors (e.g., "Director M...") are significantly more active.

##  Key Insights Summary

| Insight Category       | Key Findings                                                              |
| ---------------------- | ------------------------------------------------------------------------- |
| **Genre Focus**        | Children & Family content dominates one category; murder mystery is niche |
| **Audience Targeting** | Netflix content is heavily skewed toward teen and mature ratings          |
| **Global Reach**       | Movies show wider country participation than TV shows                     |
| **Top Contributors**   | A small number of directors contribute heavily to rated content           |
| **Content Length**     | Murder mysteries form a minor portion of total screen time                |

## Skills Demonstrated

*  Data wrangling in Power Query
*  Creating calculated columns using DAX
*  Designing an interactive, filterable report
*  Using pie charts, bar graphs, maps, and slicers effectively
*  Extracting actionable insights for business use cases

#  Use Cases for This Dashboard

*  **Marketing Strategy** – Target viewers by analyzing dominant genres and ratings.
*  **Content Licensing** – Acquire content in underrepresented categories or ratings.
*  **Regional Planning** – Understand global production for expansion opportunities.
*  **Viewer Segmentation** – Personalize recommendations using viewer preferences.

# Cleaned Dashboarrd: https://github.com/Afsha22/POWER-BI/blob/main/NETFLIX%20DATA.pbix
# Dashboard: https://github.com/Afsha22/POWER-BI/blob/main/DASHBOARD%20BI.png

