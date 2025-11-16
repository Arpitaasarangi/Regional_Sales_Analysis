 # 📈Regional_Sales_Analysis
  This project is a comprehensive analysis of Acme Co.’s sales data from 2014 to 2018, sourced from six interconnected datasets. It involves cleaning, merging, and transforming raw data       into a structured format suitable for business analysis. Through feature engineering and exploratory data analysis (EDA), the project uncovers patterns in customer behavior, product     
  performance, and regional sales dynamics. The final output includes a set of visualizations and KPIs that summarize key trends and support data-driven decision-making.
 
 ## 🎯 Project Objective
The goal is to extract actionable insights that help Acme Co. optimize its sales strategy by:
- Identifying top-performing products, regions, and sales channels
- Detecting seasonal trends and pricing anomalies
- Evaluating profitability and customer value
- Supporting strategic decisions around pricing, promotions, and market expansion
- Designing a Power BI dashboard to visualize performance metrics and guide future planning


## 📁 Dataset Breakdown :
The project uses six interconnected sheets.
- Sales Orders sheet contains columns: OrderNumber, OrderDate, Customer Name Index, Channel, Currency Code, Warehouse Code, Delivery Region Index, Product Description Index, Order Quantity,    Unit Price, Line Total, Total Unit Cost and has 64,105 rows.
- Customers sheet contains column: Customer and has 176 rows.
- Products sheet contains columns: Index, Product Name and has 31 rows.
- 2017 Budgets sheet contains columns: Product Name, 2017 Budget and has 31 rows.
- Regions sheet contains columns: ID, Name, County, State Code, State, Type, Latitude, Longitude, Area Code, Population, Households, Median Income, Land Area, Water Area, Time Zone and has
  995  rows.
- State Regions sheet contains columns: State Code, State, Region and has 50 rows.
  
## 🧰 Tools & Technologies :
- Python: pandas, numpy, matplotlib, seaborn (for data wrangling and EDA)
- Power BI: for interactive dashboard creation
- Excel: initial data source

## 🛠️ Data Preparation & Transformation :
Step-by-Step Workflow
### Data Loading & Inspection
- Loaded all six sheets into separate DataFrames
- Reviewed head() and shape to understand structure and volume
  
### Data Cleaning
- Checked for null values (none found)
- Standardized column names to lowercase and snake_case
- Removed extra spaces and dropped irrelevant columns
  
### Data Integration
- Merged Sales Orders with Customers, Products, Regions, State Regions, and 2017 Budgets using left joins
- Ensured proper key mapping across tables (e.g., customer index, product index, region index)
  
### Feature Engineering :
- Created new columns :
  total_cost = order_quantity × unit_cost
  profit = line_total − total_cost
  profit_margin_pct = (profit / line_total) × 100
- Extracted month from order_date for time-series analysis
- Filtered 2017 budget data; blanked out budget values for non-2017 records
- Aggregation & Grouping:
- Grouped data by month to calculate monthly revenue and profit
- Aggregated metrics by product, customer, region, and channel for deeper insights

## 📊 Dashboard Summary :
While the core of this project focuses on data engineering and analysis, a dashboard was created to present insights in a visually intuitive format. Below is a breakdown of the charts and their purpose:
### 🔑Key Performance Indicators (KPIs)
- Total Revenue: Overall sales revenue across all transactions
- Total Profit: Net profit after subtracting total costs
- Total Orders: Count of all sales orders
- Revenue per Order: Average revenue generated per order
- Profit Margin %: Overall profitability ratio
- 
### Visualization Charts :
- Line Chart – Monthly Revenue & Monthly Profit
Displays seasonal trends and performance over time to identify peaks and dips in sales and profitability.

- Stacked Column Chart – Order Value Distribution
Shows how order values are distributed across different ranges, helping to understand typical transaction sizes.

- Scatter Plot – Unit Price vs Profit Margin
Reveals the relationship between product pricing and profitability, highlighting pricing anomalies and margin risks.

- Stacked Bar Chart – Top 5 & Bottom 5 Customers
Compares the highest and lowest revenue-generating customers to identify key accounts and underperformers.

- Map Chart – Total Profit by State
Provides a geospatial view of profit distribution across U.S. states, highlighting regional performance.

- Donut Charts – Revenue & Profit Margin % by Region
Visualize total revenue contribution and profitability across different regions for strategic planning.

- Donut Charts – Channel-wise Profit, Revenue, and Margin per Sale
Break down performance across Online, Retail, and Distributor channels to evaluate channel effectiveness.

- Stacked Bar Chart – Top 10 Products by Revenue & Profit Margin
Identify best-selling products and those with the highest average profit margins to guide product strategy.

- Bar Chart – Top 5 States by Revenue
Ranks states based on total revenue to highlight geographic growth opportunities.

## 💡 Insights & Recommendations
- Seasonality: Clear revenue and profit peaks during specific months
- Product Strategy: High-margin products are not always top-selling — opportunity to optimize pricing
- Customer Segmentation: A small group of customers contributes disproportionately to revenue
- Channel Performance: Certain channels consistently outperform others in profitability
- Regional Focus: Some states and regions show strong potential for targeted growth









