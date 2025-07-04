# DSA_PROJECT
#Project Overview

The objective of this data analysis project is to extract actionable insights from product and customer review data, with the overarching goal of supporting strategic decision-making across key business functions.

#Dataset Description
**Data Sources**
Amazon case study.xlsx – The dataset contains 
product details: name, category, price, discount, and ratings
customer engagement: user reviews, titles, and content

https://docs.google.com/spreadsheets/d/15uM7Izb-ZDrlQLx_XSepPavA_B7BnF0x/edit?usp=drivesdk&ouid=101729043189002548095&rtpof=true&sd=true

**Data Snapshot**
Each row represents a unique product
Number of records: 1,465 rows
Number of fields: 16 columns

**Data types:**
Numerical Data-discounted_price, actual_price, discount_percentage, rating, rating_count
Categorical Data- product_id, product_name, category, user_id	, user_name, review_id
Text Data-about_product, review_title, review_content, img_link, product_link

Timeframe covered: 24 hours

**Data Cleaning & Preprocessing**
**Unnecessary Data**
Data columns such as about product, review title, review content, image link, product link, user id, and  user name were considered unnecessary to achieve the project aim, hence, were hidden.
**Missing Values**
Columns with missing data: rating
Percentage of missing values: <1%
Handling strategy (imputation of average values-2.5)
Text Preprocessing (for Category)
Split column by delimiter (|) for proper categorization

**Data Analysis**
During analysis, some extra columns were created namely: 
Number of Reviews-formula: =LEN([@[review_id]])-LEN(SUBSTITUTE([@[review_id]],",",""))+1


Price Range-formula: =IF(E2<200,"<200",IF(E2<=500,"200-500",">500"))
Pivot tables were created with pivot charts and slicers utilized where necessary

**Key Findings & Insights**
Summary of notable patterns (e.g., rating, level of discount)-no relationship
Highest performing product category in terms of potential revenue-Electronics
Lowest performing product category in terms of potential revenue-Toys & Games
Products with highest rating:
Amazon Basics Wireless Mouse | 2.4 GHz Connection, 1600 DPI | Type - C Adapter | Upto 12 Months of Battery Life | Ambidextrous Design | Suitable for PC/Mac/Laptop
Syncwire LTG to USB Cable for Fast Charging Compatible with Phone 5/ 5C/ 5S/ 6/ 6S/ 7/8/ X/XR/XS Max/ 11/12/ 13 Series and Pad Air/Mini, Pod & Other Devices (1.1 Meter, White)

**Recommendations**
Based on the EDA:
For Marketing Strategy:
Focus influencer campaigns on top-rated products
Provide discount as incentive for low performing categories such as Toys & Games
For Customer Engagement:
Address issues from negative reviews with auto-response and escalation.
Reward highly engaged customers who leave frequent reviews to encourage reviews on categories with fewer reviews namely: cars and motorbike, health and personal care, home improvement, office products, musical instruments, toys and games.
