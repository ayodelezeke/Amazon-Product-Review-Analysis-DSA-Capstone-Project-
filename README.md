# -Amazon-Product-Review-Analysis

## Table of Contents
- [Overview](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#overview)
- [Dataset](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#dataset)
- [Tool Used](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#tool-used)
- [EDA Process](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#eda-process)
  - [Data Collection](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#data-collection)
  - [Data Cleaning and Preparation](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#data-cleaning-and-preparation)
  - [Data Exploration and Analysis](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#data-exploration-and-analysis)
  - [Data Visualization](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#data-visualization)
 - [Dashboard](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#dashboard)
 - [How to Use](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#how-to-use)
 - [Key Insights](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#key-insights)
 - [Limitations](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/blob/main/README.md#limitations)

 
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
In the phase of the Data cleaning and preparation, the following actions were performed through the Power Query Editor:
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
The charts used in visualizing data insights were column and bar charts. A scatter chart was also used to show the relationship between the discount level and ratings.

## Dashboard
The features of the dashboard include:
- A complete visualization of all the insights gotten from the data in orange and black to mirror the colours of Amazon
- A slicer of product category to allow easy filtering of visuals involving the product category
- Key metrics such as the total number of products, number of product categories and the average rating of all products

A screenshot of the dashboard is included below

![Amazon Dashboard](https://github.com/user-attachments/assets/c41f32eb-2c32-4aed-9b8d-a60f7fb61673)

## How to Use
Instructions for users:
1. Download [Amazon Review.xlsx](https://github.com/ayodelezeke/-Amazon-Product-Review-Analysis/raw/refs/heads/main/Amazon%20Review.xlsx) from this repo
3. Open in Excel (desktop recommended)
4. Enable macros or content if prompted
5. Use slicers to explore the data

## Key Insights
1. The Electronics product category had the most number of products reviewed and in turn generated the highest potential revenue.
2. Looking at the relationship between discount level and rating, there is no correlation between a higher discount and rating. Product rating does not increase with discount level.
3. Looking at the correlation between number of products and price bucket range, there is an increase in the amount of products reviewed/bought with an increase in price (discounted)

## Limitations
Upon exploration of the data, it can be noticed that some distinct products share the same review id. This can affect the accuracy of conclusions made because it has a potential effect on the number of products actually reviewed.
    
