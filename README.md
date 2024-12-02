# Pizza-Sales-Analysis

### Project Overview

This project leverages Power BI to analyze one year of transactional data from Plato's Pizza. The goal is to uncover actionable insights into sales performance, customer behavior, and operational efficiency to optimize revenue growth and streamline business processes.
- Driving more sales
- Optimizing operations
- Enhancing customer satisfaction

### About Dataset

This dataset contains 4 tables, in CSV format:

A year's worth of sales from a fictitious pizza place, including the date and time of each order and the pizzas served, with additional details on the type, size, quantity, price, and ingredients.

### Data Source

Sales Data: The primary dataset used for this analysis is the "Pizza_sales_data.csv" file, containing detailed information about each sale made by the company.

### Tools

- Power BI - For creating interactive dashboards and visualizations.
- Power Query - For data transformation, Automated workflow, and integration with Power Bi

### Data Cleaning/Preparation

1. Data Loading and Importation: The data was gotten from a folder and transformed in the power query editor. In the power query editor, the table was duplicated into four and each were 
   renamed into their table names and each data was extracted by clicking the binary.
2. Data Cleaning:
   - The data was cleaned by changing the data type where needed
   - Remove Duplicates
   - Use first row as header 

### Data Modelling

Adjusted model                    
:--------------------------------:
![](![Adjusted model](https://github.com/user-attachments/assets/05f76dda-9063-4ba2-9365-252208f12d2d)
)               


The model is a Snowflakes schema.
It contains two fact tables and dimension tables


### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions, such as;

- What days and times do we tend to be busiest?
- How many pizzas are we making during peak periods?
- What are our best and worst selling pizzas?
- What's our average order value?

### Data Analysis

Data Analysis: DAX Calculations for Date Table
I generated a comprehensive date table with calculated columns to enhance time-based analysis in the data model.

1. DAX Script: Create Calendar Table
```dax 
Calendar = CALENDAR(MIN(Orders[date]),MAX(Orders[date]))
```
2. Calculated Columns in the Calendar Table
```
DAY = WEEKDAY('Calendar'[Date]
Dayname = FORMAT('Calendar'[Date], "dddd")
MONTH = MONTH('Calendar'[Date])
MONTH NAME = FORMAT('Calendar'[Date], "MMMM")
QUARTER = FORMAT('Calendar'[Date], "\QQ")
YEAR = YEAR('Calendar'[Date])
```


### Results/Findings

The analysis results are summarized as follows:
   1. Total Revenue generated 
  
   ![total revenue](https://github.com/user-attachments/assets/b4e183f4-73b3-4fd9-91ec-ec4833ffed69)

   2. Average Order Value

    
    

  ![average order value](https://github.com/user-attachments/assets/c71e0153-717b-4e24-9f10-424210fb3015)


   3. Top Categories: The pizza category which is most in demand is the **Classic**  
   4. Peak Sales Hours: The highest number of pizzas were sold at 12:00 PM
   8. The busiest time of the day is between **12pm and 1pm** which is Lunch period.
   9. The busiest days are **Fridays and Saturdays** (Beginning of the weekend).
   10. Our overall best selling pizza is The **Classic Deluxe Pizza**
   11.  The worst selling pizza is The **Brie Carre Pizza**
   12.  The highest sold pizza size is the **Large Size**
     

 ### Visualization 

 Interact with the Dashboard [here](https://app.powerbi.com/groups/me/reports/b80abe4a-d77b-4ad5-8468-425057ed5d3c?ctid=48aeb350-11ea-46b3-9859-dd5b56f8bc21&pbi_source=linkShare)
  
  
  
 
  
  ![Pizza_Sales_Dashboard](https://github.com/user-attachments/assets/2c5975f8-77f6-4170-9935-fc3917409ed6)

  
  ### Recommendation


  Based on the analysis, i recommend the following actions:

1. Highlight top-selling pizzas and opportunities for upselling in advertising efforts. These goods make up a significant portion of sales. You can boost sales by concentrating on what your customers like without increasing your marketing budget.Incorporating these pizzas into the "Customer Favorites" sections of the menu and offering combo packages that combine them with pricey items like drinks or desserts are two ways to do this.Goal Off-Peak Hours

2. Put temporary discounts or specials into effect. Sales during off-peak hours are significantly lower, thus the cooking and delivery operations are operating at underused capacity.
 Use social media and loyalty programs to let customers know about these deals. This brings in more cash without disrupting business operations during busy hours.

3. Make operations more efficient during busy periods. Increase worker levels and streamline preparation processes at busy times (e.g., weekends and evenings).
  According to the data, preparation and delivery times are longer during times of high demand, which could annoy customers. Put in place a more flexible scheduling system and get components that are in high demand ready beforehand.

4. Give back to loyal customers. Start a loyalty program that gives out freebies or discounts to customers who make a specific number of transactions. Strong brand loyalty is demonstrated by the [X]% of total orders that come from repeat customers. Word-of-mouth advertising and lifetime value are increased when their experience is improved. Utilize data to pinpoint loyal customers and provide them tailored offers through email or app alerts.

5. Encourage Participation with Seasonal Themes. Introduce time-limited promotions that correspond with holidays or seasons, such as "Winter Delight" or "Summer BBQ Pizza."  Seasonal discounts increase client attention and orders during times of transition by generating a sense of urgency and enthusiasm. Use digital advertisements, email marketing, and social media campaigns to promote seasonal products.




  
     


              

