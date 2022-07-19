# Airplane Crahes Analysis Since 1908
This project was made in pursuant to #NG30DAYSOFLEARNING.
The dashboard is published in the Power Bi service - [Air crash analysis](https://app.powerbi.com/groups/me/reports/099521ef-708e-4ff1-8183-a362b490dec6/ReportSection)


## Objective.
-   The main objective of having this project is to analayze and discover patterns about airplane crashes globally since 1908-2009. From my own point of view, I see this project as being more of exploratory than other forms of mining the data. And this has made my thought process while questioning the data. The questions asked are:
    1. What is the trend of crahes over time?
    2. What was the fatality rate?
    3. What is the overall survival rate?
    4. How has the survial and fatality rate been oner the years?
    5. what were the major causes of these crashes?
    6. Which location recorded the a lot of fatalities?

-   The  analytical process was further subdivided in parts that captures the analytical process. They include:
    -	Data Gathering
    -	Data Cleaning
    -	Data Transformation
    -	Data Visualization
    -	Insights or takeaways

### Data Gathering
This data was collected from the Kaggle’s site- Airplane Crashes Since 1908 (url). It contains (no) fields and (no.) Rows. The fields are Date, Time, Location, Route, Summary, Aboard, Fatalities etc (picture)1
************

### Data Modelling
**************

### Data Cleaning
Since this is the most fundamental step in data analysis. The cleaning process include:
    - Checking, verifying and changing data inconsistent with their respective fields.
    - Removed columns whose null values are more than 30% which my hinder the analysis and seem not necessary with the dashboard objective
- Removed Duplicate values in the provided dataset.
• Inside the Power Query, I splitted the Location column with the comma delimeter to get the leftmost characters after the delimeter

***************

### Data Transformation
-	To ensure grannulrity, I splitted the DATE column with the Date functions in Power Query. Afterwards, a hierarchy was built out of the separates column in Power Bi Desktop.
-	A new column was created with DAX Expression named Survival to get the number of persons who were alive. The result was brought about by the subtraction of the fatalities field from the Aboard field.
-	A new measure was created with a Dax Expression to get both the survival rate and fatality rate.

******************

### Conclusion.