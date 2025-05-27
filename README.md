# YELP-Review-Analysis
This project focuses on analyzing large-scale review data from the Yelp website, covering various businesses across multiple categories. The dataset was downloaded in JSON format, preprocessed, and stored in AWS S3 for scalability and accessibility. Using Snowflake, the data was ingested, transformed, and analyzed efficiently.

## 🔧 Project Development Process

### 1. Requirement Gathering & Objective Definition
- Identified analytical goals: sentiment trends, popular categories, user behavior, business performance, etc.  
- Business questions relevant to stakeholders (e.g., review volume, average ratings, top businesses).

### 2. Data Acquisition
- Downloaded Yelp's public dataset in **JSON** format, which includes data on businesses, reviews, users, and check-ins.

### 3. Data Storage in AWS S3
- Uploaded raw JSON files to **Amazon S3** for secure, scalable, and cost-effective storage.  
- Structured S3 buckets for easy versioning, access, and future data integration.

### 4. Data Ingestion with Snowflake
- Configured **external stages** in Snowflake to connect with the S3 bucket.  
- Used **Snowpipe** or bulk `COPY INTO` commands to load JSON data into Snowflake tables efficiently.

### 5. Data Transformation & Modeling
- Parsed semi-structured JSON using Snowflake’s `FLATTEN`, `LATERAL`, and `VARIANT` support.  
- Normalized data into analytical **fact** and **dimension** tables.  
- Joined datasets (reviews, businesses, users) to create a unified analytical model.

### 6. Data Cleaning & Quality Checks
- Removed duplicates, handled missing values, and standardized formats (e.g., dates, locations).  
- Ensured data integrity through consistency checks across tables and joins.

### 7. Exploratory Data Analysis (EDA)
- Performed SQL-based analysis to uncover trends in reviews, ratings, business types, and user behavior.  
- Used temporary views and CTEs to iteratively explore data insights.

### 8. Insight Generation & Reporting
- Derived key metrics: average ratings per category, top-performing cities, frequent reviewers, sentiment trends.  

### 9. Scalability & Optimization
- Applied clustering keys, query profiling, and data partitioning in Snowflake for performance tuning.  
- Ensured that the pipeline supports future automation and scaling as data grows.

## 🔍 Real-World Problem Statements Solved
As part of the Yelp Reviews Analysis, the following real-world data challenges were addressed using SQL queries on the Snowflake platform:

**1. Number of businesses in each category**
- Helps understand the distribution and dominance of business types on Yelp.

**2. Top 10 users who reviewed the most businesses in the restaurant category**
- Identifies highly active users and potential influencers in the food industry.

**3. Most popular business categories (based on number of reviews)**
- Reveals which types of businesses receive the most customer engagement.

**4. Top 3 most recent reviews for each business**
- Useful for tracking latest customer sentiments and recent service performance.

**5. Month with the highest number of reviews**
- Highlights seasonal trends or marketing impact.

**6. Percentage of 5-star reviews for each business**
- Indicates customer satisfaction levels and quality perception.

**7. Top 5 most reviewed businesses in each city**
- Identifies local hotspots and high-traffic businesses.

**8. Average rating of businesses with at least 100 reviews**
- Ensures statistical significance in evaluating consistent performers.

**9. Top 10 users who wrote the most reviews and the businesses they reviewed**
- Shows user engagement and review patterns.

**10. Top 10 businesses with the highest number of positive reviews**
- Helps pinpoint top-rated businesses with strong reputations.

**These questions were selected to demonstrate practical, real-world data insights for business strategy, marketing, and customer behavior analysis.**
