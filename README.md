# -Amazon-Product-Review-Analysis
 
## Overview
An Exploratory Data Analysis into product and customer review data from Amazon to generate insights that can guide product improvement, marketing strategies, and customer engagement.

## Dataset
The dataset contains information scraped from Amazon product pages, including: 
- Product details: id, name, category, price, discount, and ratings 
- Customer engagement: user reviews, titles, and content 

Each row represents a unique product, with aggregated reviewer data stored as comma-separated values 

Format: XLSX

Total Records: 1,465 rows, 16 columns

## Tool Used
MS Excel [Download Here](https://www.microsoft.com/en-us/microsoft-365/excel)
- Pivot Tables (For data summarization)
- Charts (For visualization)
- Conditional Formatting (To check for duplicates)
- Power Query (For data cleaning)


## EDA Process
The Exploratory Data Analysis process involves working with the data to generate insights that can provide value and clarity and it starts with:

### Data Collection
The data contained within the dataset was scraped from Amazon pages

### Data Cleaning and Preparation
In the phase of the Data cleaning and preparation, we perform the following actions through the Power Query Editor:
  1. Data loading and inspection
  2. Removal of duplicates
  3. Handling missing variables
  4. Data type conversions
  5. Data cleaning and formatting

### Data Exploration and Analysis
Further exploration and analysis of the Data involves answering these questions:
1. What is the average discount percentage by product category? 
2. How many products are listed under each category? 
3. What is the total number of reviews per category?  
4. Which products have the highest average ratings? 
5. What is the average actual price vs the discounted price by category? 
6. Which products have the highest number of reviews? 
7. How many products have a discount of 50% or more? 
8. What is the distribution of product ratings? 
9. What is the total potential revenue by category? 
10. What is the number of unique products per price range bucket? 
11. How does the rating relate to the level of discount? 
12. How many products have fewer than 1,000 reviews? 
13. Which categories have products with the highest discounts? 
14. Identify the top 5 products in terms of rating and number of reviews combined.

To answer these questions, the data summarization tool (Pivot Table) was used. Questions concerning averages, summation, count etc. of columns, rows and cells were answered through this tool. Filtering and reorganizing data already summarized was also possible due to its interative nature. 

Some questions however were answered through the use of excel formulas. For example the question - How many products have a discount of 50% or more? was answered through this use. The steps to answering this question are:
1. Create a calculated column: This column states "Yes" or "No" if a product has a discount percentage equal to or above 50% using the excel formula
``` EXCEL
=IF([@[discount_percentage]]>= 50%, "Yes", "No")
``` 
2. Getting insight based on the calculated column: Counting the amount of "Yes" in the calculated column using the excel formula on the answer worksheet
``` EXCEL
=COUNTIF(Table1_1[discount_percentage above 50%], "Yes")
```
### Data Visualization


    
