
# 📊 Amazon Product Data Analysis — DSA Project

## 🔍 Project Overview

The objective of this data analysis project is to extract actionable insights from product and customer review data, with the overarching goal of supporting strategic decision-making across key business functions.

---

## 📁 Dataset Description

### 📌 Data Source

- **Filename**: `Amazon case study.xlsx`

### 🧾 Contents

- **Product Details**: Product name, category, price, discount, ratings
- **Customer Engagement**: User reviews, titles, and content

### 🔢 Data Snapshot

- **Number of records**: 1,465 rows
- **Number of fields**: 16 columns

### 🧬 Data Types

- **Numerical**: `discounted_price`, `actual_price`, `discount_percentage`, `rating`, `rating_count`
- **Categorical**: `product_id`, `product_name`, `category`, `user_id`, `user_name`, `review_id`
- **Text**: `about_product`, `review_title`, `review_content`, `img_link`, `product_link`

### ⏱ Timeframe Covered

- 24 hours

---

## 🧹 Data Cleaning & Preprocessing

### 🗑 Unnecessary Data

The following columns were hidden for analysis due to irrelevance to the project's objectives:
- `about_product`, `review_title`, `review_content`, `image_link`, `product_link`, `user_id`, `user_name`

### ❓ Missing Values

- **Column with missing data**: `rating`
- **Percentage missing**: <1%
- **Handling strategy**: Imputation using average rating (2.5)

### 🏷 Text Preprocessing

- `category` column was split by delimiter `|` for proper classification

---

## 📈 Data Analysis

### 🧮 Created Columns

- **Number of Reviews**:  
  `=LEN([@[review_id]])-LEN(SUBSTITUTE([@[review_id]],",",""))+1`

- **Price Range**:  
  `=IF(E2<200,"<200",IF(E2<=500,"200-500",">500"))`

### 📊 Tools Used

- Pivot tables
- Pivot charts
- Slicers for data exploration

---

## 📌 Key Findings & Insights

- **No correlation** between rating and level of discount
- **Top performing category**: Electronics (by potential revenue)
- **Lowest performing category**: Toys & Games

### 🌟 Products with Highest Ratings:

- **Amazon Basics Wireless Mouse**  
  _2.4 GHz, 1600 DPI, Type-C Adapter, 12-month battery, Ambidextrous_

- **Syncwire LTG to USB Cable**  
  _Compatible with most Apple devices, 1.1 Meter, White_

---

## 💡 Recommendations

### 📣 For Marketing Strategy:

- Focus influencer campaigns on **top-rated products**
- Offer **discounts on low-performing categories** (e.g., Toys & Games)

### 👥 For Customer Engagement:

- Address issues in negative reviews with **auto-response/escalation**
- Reward highly engaged reviewers to **boost review volume** in underrepresented categories:
  - Cars & Motorbike
  - Health & Personal Care
  - Home Improvement
  - Office Products
  - Musical Instruments
  - Toys & Games
---

## 🧠 Author

**Ayomide Oguntodu**  
_Lead Analyst – DSA Amazon Case Study Project_

