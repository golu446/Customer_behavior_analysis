Customer Shopping Behavior Analysis

Project Overview
This project analyzes customer shopping behavior using 3,900 purchase
records and 18 columns. The goal is to understand customer
spending, product preferences, discounts, subscription behavior, and
purchasing patterns to support better business decisions.
Tools & Technologies
- Python --- data cleaning and preparation
- Pandas --- data loading, exploration, and transformation
- PostgreSQL --- SQL-based business analysis
- Power BI --- interactive dashboard and visualizations
Dataset Overview
The dataset contains 3,900 rows, with one row per purchase, and 18
columns covering:
- Customer information: age, gender, location, subscription status
- Purchase details: item, category, purchase amount, season, size,
  color
- Shopping behavior: discounts, previous purchases, purchase
  frequency, review rating, shipping type, and payment method
There were 37 missing review ratings. These were filled using the
median review rating for each product category. Column names were
standardized to lowercase with underscores. Two additional fields were
created: - age_group - purchase_frequency_days
The promo_code_used column was removed because it duplicated the
information in discount_applied.
Project Workflow
1. Load and explore the dataset using Pandas.
2. Review dataset structure and descriptive statistics.
3. Handle missing review ratings using category-level medians.
4. Standardize column names.
5. Create age groups and convert purchase frequency into days.
6. Remove the duplicate promo_code_used field.
7. Load the cleaned data into PostgreSQL.
8. Use SQL queries to answer business questions.
9. Build an interactive Power BI dashboard.
Business Questions Answered
The analysis explores ten questions:
1. Which gender generates more revenue?
2. Which customers use discounts and still spend above the average
   purchase amount?
3. Which five products have the highest average ratings?
4. Do customers spend more with Standard or Express shipping?
5. Do subscribers spend more than non-subscribers?
6. Which products have the highest discount rates?
7. How many customers are New, Returning, or Loyal?
8. What are the three most purchased products in each category?
9. Are frequent buyers (more than five previous purchases) more likely
   to subscribe?
10. Which age group generates the most revenue?
Key Findings
- Revenue by gender: Male customers generated approximately
  $157,890, compared with $75,191 from female customers.
- Discount users: 839 customers used a discount and spent more
  than the average purchase amount.
- Top-rated products: Gloves (3.86), Sandals (3.84), Boots (3.82),
  Hat (3.80), and Skirt (3.78).
- Shipping: Average purchase amount was approximately $60.48 for
  Express shipping and $58.46 for Standard shipping.
- Subscriptions: 1,053 customers subscribed and 2,847 did not.
  Average spend was about $59.49 for subscribers and $59.87 for
  non-subscribers.
- Products frequently discounted: Hat (50.00%), Sneakers (49.66%),
  Coat (49.07%), Sweater (48.17%), and Pants (47.37%).
- Customer segments: 3,116 Loyal, 701 Returning, and 83 New
  customers.
- Frequent buyers: Among customers with more than five previous
  purchases, 2,518 were non-subscribers and 958 were subscribers.
- Revenue by age group: Young Adults generated $62,143, followed
  by Middle-aged ($59,197), Adult ($55,978), and Senior ($55,763).
Power BI Dashboard
The interactive dashboard highlights: - Approximately 3,900
customers - Average purchase amount: $59.76 - Average review
rating: 3.75/5 - Subscription split: 27% subscribed and 73%
not subscribed - Revenue and sales by category and age group - Filters
for subscription status, gender, category, and shipping type
Recommendations
- Encourage subscriptions: Test meaningful benefits such as
  exclusive deals or free shipping.
- Reward loyal customers: Create a loyalty program and encourage
  Returning customers to become Loyal customers.
- Review discount effectiveness: Evaluate whether high discount
  rates are reducing profit margins.
- Promote popular products: Feature highly rated products and
  category bestsellers in marketing campaigns.
- Improve targeted marketing: Focus on high-revenue age groups,
  consider Express shipping preferences, and investigate opportunities
  to grow female-customer revenue.
Repository Structure
A suggested structure for this project is:
Customer-Shopping-Behavior-Analysis/
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   └── customer_shopping_behavior_analysis.ipynb
├── sql/
│   └── customer_shopping_behavior.sql
├── powerbi/
│   └── customer_behavior_dashboard.pbix
└── README.md
Update the filenames and folders above to match the files included in
your repository.
How to Run
1. Clone or download this repository.
2. Install Python and the required libraries, such as Pandas.
3. Open the analysis notebook in Jupyter Notebook or Google Colab.
4. Run the data-cleaning and preparation steps.
5. Import the cleaned data into PostgreSQL and execute the SQL analysis
   queries.
6. Open the .pbix file in Power BI Desktop to explore the dashboard.
Note: The source project description does not specify the exact
dataset filename, notebook filename, SQL script filename, or database
connection settings. Adjust the example structure and instructions to
match your actual project files.
