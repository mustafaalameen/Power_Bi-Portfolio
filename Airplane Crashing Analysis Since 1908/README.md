# Airplane Crahes Analysis Since 1908
This project was made in pursuant to #NG30DAYSOFLEARNING.
The dashboard is published in the Power Bi service - [Air crash analysis](https://app.powerbi.com/groups/me/reports/099521ef-708e-4ff1-8183-a362b490dec6/ReportSection)

![Screenshot (273)](https://user-images.githubusercontent.com/70868527/179970535-4c646033-f956-4773-894b-5e4649d4d15a.png)
![Screenshot (272)](https://user-images.githubusercontent.com/70868527/179970675-c3a83d40-9721-4ebb-acd0-1e35d1f9c8d9.png)

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
This data was collected from the Kaggle’s site- Airplane Crashes Since 1908 (https://aka.ms/30DLDATGitHubRepo). It contains  fields and 5197 Rows. The fields are Date, Time, Location, Route, Summary, Aboard, Fatalities etc 
![Screenshot (280)](https://user-images.githubusercontent.com/70868527/179979095-46231f02-7a8a-4109-ac3c-767a4d22b9e3.png)
************

### Data Modelling
 Apart from the dataset imported  into the data model, I created another new table called DATE using the DAX expression in other to optimize performance of the visuals and quereies made to the main table. For easy easy filtering i used a one - many relationship between the date table and the imported table 

![Screenshot (270)](https://user-images.githubusercontent.com/70868527/179972776-a9f2d49c-0692-458a-b2a9-282e2ac09fd2.png)
**************

### Data Cleaning
Since this is the most fundamental step in data analysis. The cleaning process include:
    - Checking, verifying and changing data inconsistent with their respective fields.
    - Removed columns whose null values are more than 30% which my hinder the analysis and seem not necessary with the dashboard objective
- Removed Duplicate values in the provided dataset.
- Inside the Power Query, I splitted the Location column with the comma delimeter to get the leftmost characters after the delimeter

***************

### Data Transformation
-	To ensure grannulrity, I splitted the DATE column with the Date functions in Power Query. Afterwards, a hierarchy was built out of the separates column in Power Bi Desktop.
-	A new column was created with DAX Expression named Survival to get the number of persons who were alive. The result was brought about by the subtraction of the fatalities field from the Aboard field.
-	A new measure was created with a Dax Expression to get both the survival rate and fatality rate.
-	A tooltip was created for further infomation like the filtered Year, No. of crashes and Number of fatalities and survival.
![Screenshot (281)](https://user-images.githubusercontent.com/70868527/179979689-e6c06d76-caf2-4965-931f-c10740bc8339.png)

******************
### Insights and Takeaways
1.  Fatality rate seems to be on the rise and unbearable.
    ![Screenshot (278)](https://user-images.githubusercontent.com/70868527/179975218-26a611f4-1ab3-4f47-a2b4-8cb6eb762ac4.png)
    
2.  The survival rate over time is very low which signifies that one is at risk of not been safe even in recent times (after 2000).
    ![Screenshot (279)](https://user-images.githubusercontent.com/70868527/179975281-b7b54a08-ec66-4fda-a354-52b189d5a634.png)
    
3.  Aeroflot and The Military - U.S Air force equally had the highest number of crashes between 1908 - 2009.
    ![Screenshot (276)](https://user-images.githubusercontent.com/70868527/179976895-77e7b28e-ba41-491f-b638-9e7e3c9b9158.png)

4.  Apparently, Brazil and Alaska are locations that recorded the most number of crashes while Columbia had the highest fatality rate.
    ![Screenshot (277)](https://user-images.githubusercontent.com/70868527/179976879-f7023d4e-1d65-4f92-a183-4f4ffed12dbc.png)

5.   The number of crashes increased radically  between 1976 -1979. Notably, the highest was recorded in 1972 with 103 airplane crashes with 80.96% fatality rate with      a very low survival rate. Then, it can claimed to be the most turbulent  period on earth.
     ![Screenshot (282)](https://user-images.githubusercontent.com/70868527/179980293-32a22e7a-1971-4015-a7ee-e2ab802ae3a7.png)

### Conclusions.
    That's a wrap! Futher changes may be made in the future as I forge ahead in learning PowerBi.
