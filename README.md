## Amazon-Product-Analysis
This project explores a dataset of Amazon product reviews. It includes data cleaning, exploratory data analysis (EDA), and visualizations using Microsoft Excel. The goal is to uncover insights into customer sentiment, rating patterns, and product performance.

### Project Overview
While working as an Analyst at Retail Tech Insights,a company focused on e-commerce analytics for Amazon sellers. I conducted analysis on products, examining performance and customer review data. The objective of this project is to uncover actionable insights that can support:
-  Product improvement by identifying common customer pain points and satisfaction drivers
-  Marketing strategies by highlighting top-performing products and review sentiment trends
-  Customer engagement by understanding feedback patterns and review behavior
This analysis leverages Microsoft Excel for data cleaning, exploratory data analysis (EDA), and visualization. The findings aim to help Amazon sellers make data-informed decisions that enhance product offerings, optimize marketing efforts, and improve customer 
### Dataset Overview
This 1456 rows and 16 colunms dataset contains product and review data for items sold on Amazon. It includes pricing, discount levels, customer ratings, and estimated revenue metrics.
### Key Columns
| Column Name           | Description |
|-----------------------|-------------|
| `Product_id`          | Unique identifier for each product |
| `Product_name`        | Name of the product |
| `Category`            | Product category |
| `Discounted_price`    | Final selling price after discount |
| `Actual_price`        | Original price before discount |
| `Discount_percentage` | Proportion of discount applied |
| `Rating`              | Average customer rating (out of 5) |
| `Rating_count`        | Number of ratings received |
| `Review_id`           | Unique identifier for each review |
| `Price_bucket`        | Price range category |
| `Potential_revenue`   | Estimated revenue (Discounted Price × Rating Count) |
| `Discount`            | Discount level (High, Medium, etc.) |
| `Rating_Score`        | Weighted score (Rating × Rating Count) |

###  Tools Used
- Microsoft Excel (for data cleaning and visualization)

###  Analysis Objectives
- Identify top-rated and low-rated products
- Analyze review volume and rating distribution
- Detect patterns in customer sentiment
- Explore correlations between review length, rating, and helpfulness

###  Data Cleaning Summary
This document outlines the steps taken to clean and prepare the Amazon product review dataset for analysis using Microsoft Excel.
###  Cleaning Steps
- **Used Delimiter Tool**:  
  Split combined columns using Excel’s delimiter feature to separate values cleanly (e.g., product names, Category,Review ID)
- **Standardized Text Columns**:  
  - Removed inconsistent spacing and capitalization in columns
  - Ensured consistent formatting for easier grouping and filtering.
### Calculated Columns
Created four new columns to enhance analysis:
1. **Price Bucket**  
   Categorized products into price ranges (e.g., `₹200–500`, `>₹500`) based on `Discounted_price`.
2. **Discount**  
   Classified discount levels (e.g., `High`, `Medium`) based on `Discount_percentage`.
3. **Potential Revenue**  
   Estimated revenue using the formula:  
   `Potential_revenue = Discounted_price × Rating_count`
4. **Rating Score**  
   Weighted product popularity and quality using:  
   `Rating_Score = Rating × Rating_count`
   
This section outlines the 14 key questions explored during the analysis, along with the tools used, methods applied, and insights discovered.
### Exploratory Data Analysis (EDA Summary)

This table summarizes the 14 key questions explored during the analysis of Amazon product review data, including the tools used, methods applied, and insights gained.

|  No. |  Question                                                                 | Tool Used            |  Method                                                                                  |  Insight                                                                                   |
|-------|------------------------------------------------------------------------------|--------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 1     | What is the average discount percentage by product category?                | PivotTable               | Grouped by `Category`, averaged `Discount_percentage`                                       | *Computers & Accessories* had the highest average discounts (60%+)                          |
| 2     | How many products are listed under each category?                           | PivotTable               | Counted unique `Product_id` values grouped by `Category`                                    | Dataset is focused on *Computers & Accessories*                                              |
| 3     | What is the total number of reviews per category?                           | PivotTable               | Summed `Rating_count` by `Category`                                                         | *Computers & Accessories* had the highest total reviews                                      |
| 4     | Which products have the highest average ratings?                            | PivotTable               | Averaged `Rating` per product, sorted descending                                             | Several products rated above 4.5                                                             |
| 5     | What is the average actual vs. discounted price by category?                | PivotTable               | Averaged `Actual_price` and `Discounted_price` by `Category`                                | Discounts were significant across all categories                                             |
| 6     | Which products have the highest number of reviews?                          | Sort                     | Sorted `Rating_count` column in descending order                                             | *Boat Deuce USB* and *Ambrane 60W* had the most reviews                                      |
| 7     | How many products have a discount of 50% or more?                           | Filter                   | Filtered `Discount_percentage >= 0.50`                                                       | Many products offered 50%+ discounts                                                         |
| 8     | What is the distribution of product ratings?                                | PivotTable + Grouping    | Grouped `Rating` into bins (e.g., 3.0–3.5, 3.5–4.0), counted frequency                       | Most products rated between 3.5 and 4.5                                                      |
| 9     | What is the total potential revenue by category?                            | PivotTable               | Summed `Potential_revenue` by `Category`                                                    | *Computers & Accessories* generated the highest revenue                                      |
| 10    | What is the number of unique products per price range bucket?              | PivotTable               | Counted unique `Product_id` values grouped by `Price_bucket`                                | Most products fall into ₹200–₹500 and >₹500 buckets                                          |
| 11    | How does the rating relate to the level of discount?                        | PivotTable               | Grouped by `Discount`, averaged `Rating`                                                    | High-discount products still had strong ratings (4.0+)                                       |
| 12    | How many products have fewer than 1,000 reviews?                            | Filter                   | Filtered `Rating_count < 1000`                                                              | Many products had low visibility or were newly listed                                        |
| 13    | Which categories have products with the highest discount percentages?       | PivotTable               | Grouped by `Category`, calculated max and average `Discount_percentage`                     | *Computers & Accessories* had several products discounted over 80%                           |
| 14    | Identify the top 5 products by rating × number of reviews (Rating Score)    | Calculated Column + Sort | Created `Rating_Score = Rating × Rating_count`, sorted descending                           | Top products had high ratings and massive review counts—ideal for promotion                  |
  


### VISUALS

![DASHBOARD](https://github.com/user-attachments/assets/0b92f16c-4ccb-4ff4-baa9-755d6f961837)





![Cleaned Data](https://github.com/user-attachments/assets/b8d60b8b-97c6-44a4-af76-996bb9aba7bb)


![Raw dataset](https://github.com/user-attachments/assets/5343e0b4-d14f-46c1-8b78-e655018e1916)



### Insights & Recommendations

This section summarizes the key findings from the analysis of Amazon product review data, based on the Excel dashboard created during the project.

###  Key Insights

### 1. Top Revenue Drivers
- Products like **Boat Deuce USB** and **Ambrane Unbreakable 60W** generate the highest potential revenue.
- These products combine high review volume with competitive pricing, making them strong performers in both sales and customer engagement.

### 2. Price Buckets & Performance
- The majority of products fall into the `₹200–500` and `>₹500` price buckets.
- These segments show strong average ratings (4.0+), indicating that customers are satisfied with mid-range and premium-priced products.

### 3. Discount Strategy
- Products with **High Discounts** (up to 90%) still maintain solid ratings.
- This suggests that aggressive discounting can drive volume without negatively impacting customer satisfaction—an opportunity for promotional campaigns.

### 4. Rating Score as a Composite Metric
- The `Rating_Score` (Rating × Rating_count) highlights products that are both popular and well-reviewed.
- This metric is useful for prioritizing products in marketing, inventory planning, and customer targeting.

### 5. Category Focus
- All products analyzed fall under **Computers & Accessories**, with a strong presence of USB cables and charging accessories.
- This indicates a high-demand subcategory that sellers can focus on for bundling, upselling, or cross-promotion.

### Recommendations

This Amazon product review analysis for RetailTech Insights provides a comprehensive understanding of product performance, pricing dynamics, and customer engagement across various categories.
- **Use discounts strategically** to boost volume without compromising product perception.
- **Target mid-range price buckets** in marketing campaigns, as they show the best balance of value and satisfaction.
- **Monitor review trends** to identify emerging issues or opportunities for product improvement.

