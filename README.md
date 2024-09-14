### Languages and Tools

- **R**: For data wrangling, cleaning, and analysis.
- **RMarkdown**: For generating reproducible reports.
- **Excel**: The original data source, processed using `readxl` in R.

# Data Wrangling and Offense Data Analysis for Australia

## Overview

This project is divided into two parts, focusing on data wrangling and the analysis of Australian offense data over multiple years. The dataset includes offenses categorized by type and gender, spanning over several years. The goal of the project is to clean and tidy the dataset, handle missing values and outliers, and create new features for deeper insights into crime trends.

### Part 1: Offenses Data Preprocessing and Analysis

In the first part, the project focuses on tidying and manipulating the dataset to make it suitable for analysis. Several steps were taken to clean the data, handle missing values, and create new variables that provide additional insights into crime patterns. These steps include:

1. **Data Import and Cleaning**:
   - The data was imported from multiple Excel sheets, which included offense categories, subcategories, and data divided by gender.
   - Functions like `class()`, `dim()`, `str()`, and `as.factor()` were used to understand the data structure and ensure attributes were in the correct format.

2. **Data Tidying**:
   - The dataset initially had years as column headers, which violated the principles of tidy data.
   - The `gather()` function was used to transform the dataset into a tidy format, with offense categories as variables and years as observations.

3. **New Feature Creation**:
   - Two new attributes, `gender_percentage` and `offense_rate`, were created to provide deeper insights into the distribution of crimes by gender and over time.
   - These new features were derived by calculating the percentage of offenses per category and the rate of offenses per gender.

4. **Handling Outliers and Skewness**:
   - Outliers were detected and handled by replacing them with appropriate values based on the distribution of the data.
   - Skewed data distributions were log-transformed to normalize the data and ensure accurate analysis.

5. **Scan and Analysis**:
   - Missing values, special values, and inconsistencies were checked across the dataset.
   - The results showed that gender-specific offense data had missing values due to human error in the dataset. These errors were fixed by adjusting the offense numbers based on calculated percentages.

### Part 2: (Code Missing)

The second part of the project involves further analysis and visualization of the offense data. Unfortunately, the code for this part is missing. However, the goal of this section was to perform advanced analysis, including:

- Visualizing trends in the offense data.
- Creating predictive models to analyze future trends in crime rates.
- Exploring correlations between different offense types and demographic factors.

### Files in the Repository

- **`report.pdf`**: The detailed report for Part 1, including data cleaning, feature creation, and outlier handling.
- **`report2.pdf`**: The report for Part 2, outlining the intended analysis and steps taken, though the source code is missing for this part.
- **`code.Rmd`**: RMarkdown file containing the code for Part 1, used for tidying the data, creating new features, and handling outliers.
- **`data.zip`**: Contains the raw dataset used for the analysis in both parts.

### How to Run the Project

1. **Set Up RStudio**:
   - Open the `code.Rmd` file in RStudio to run the analysis for Part 1 of the project.
   - Ensure you have the necessary packages installed, such as `tidyverse` and `readxl`.

2. **Data**:
   - The dataset is included in the `data.zip` file. Unzip and place the data files in the same directory as the `code.Rmd` file to run the code seamlessly.

### Data Source

The dataset used for this project is from the **Australian Bureau of Statistics** and includes offense data categorized by year, type of offense, and gender.
