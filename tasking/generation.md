# workflow

# Question / prompts

## A. Factual Responses for Given Data

## 1. Description

- **Hey, can you give me the distribution of salary for employees older than 30 in the salary.csv file I provided?**
- how many columns in the dataset from the CSV file contain outliers?
- how many columns in the dataset from population.xls contain negative values?
- how many columns in the dataset from population.csv contain empty strings?
- tell me the number of columns in the dataset that have only one ASCII character from the CSV?
- tell me the number of columns in the dataset which have null values?

2. Retrieval

   - **“What is the inventory value on 03/10/20 for the widget product”**
   - **“What were John Smith’s hours worked last Tuesday”**

3. Filtering
   - **“Show me all the appointments I had for mens haircuts last week”**
   - show me the names of all columns that contain prices below 100
   - display the names of all columns that contain prices with significant deviations
   - display the names of all columns that contain prices with deviations close to zero

## B. Straight Forward Requests

1. Data Cleaning

   - **“Replace all empty cells in column x with 0”**
   - **“Update all the dates in the app time column to be in mm dd yy format”**
   - **“Make sure all the data in the cost column is formatted as a number, and not a string”**
   - **"Remove duplicate entries and fill in missing values in the original sales transaction data."**
   - Ensure that the Amount column is formatted as a number and converted to grams from kilograms.
   - Convert the Margin column to a floating-point format and transform it from a percentage to a decimal.

2. Identify errors

   - **“Show me records that are missing x column”**
   - **“Show me records with duplicate sales ID values”**
   - **Show me all the rows where column x is null**
   - **“Are there any format differences in columns x, y, and z”**
   - check if there are any outliers in the TRANSPORTATION and GASOLINE columns of the CSV file?
   - display all the records that have a total column greater than the mean value.

3. Data TransformationData Transformation (Generate aggregation table)

   - **"Create a table showing the total sales, average order value, and number of orders for each product category."**
   - **“Show me avg selling price by color in a table”**

   - What is the total sum of values in Column A grouped by categories in Column B?
   - What is the average value of Column A for each unique value in Column B?
   - What is the maximum value in Column A corresponding to the minimum value in Column B?
   - What is the total count of records where Column A meets certain conditions and Column B meets different conditions?
   - What is the median value of Column A for each distinct value in Column B?
   - What is the sum of Column A for each month or year, aggregated by the values in Column B?
   - What is the average value of Column A for each combination of values in Columns B and C?
   - What is the standard deviation of values in Column A for each category in Column B?
   - What is the correlation coefficient between Column A and Column B?
   - What is the proportion of records where Column A exceeds a certain threshold, grouped by ranges of values in Column B?

4. Data Transformation (computed columns)

   - **"Generate a table with a new column calculating the profit margin for each transaction based on the product cost and selling price.**
   - Calculate the total revenue by multiplying the unit price by the quantity sold for each item.
   - Create a new column that computes the profit margin by subtracting the cost from the revenue.
   - Determine the age of individuals based on their birthdate and the current date.
   - Compute the BMI (Body Mass Index) using height and weight data.
   - Derive a new column indicating whether a customer is a high-value customer based on their purchase history.
   - Generate a new column categorizing customers into segments based on their spending habits or purchase frequency.
   - Calculate the cumulative sum of sales for each month.
   - Create a new column indicating whether a product is out of stock based on its inventory level.
   - Compute the average rating for each product based on customer reviews.
     Derive a column indicating the season of the year based on the date.

5. (M) Data Transformation (Join Tables)

   - **"Merge table X and Y on key Z"**
   - **“Add the data from [file name a] to [file name b] and join on column x and y”**
   - **"Show rows in X that don't match rows in Y, using Z"**
   - Merge two tables based on a common key or attribute.
   - Combine customer information from one table with their transaction history from another table.
   - Join employee data with department information to analyze employee distribution across departments.
   - Merge sales data with product information to analyze sales performance for each product.
   - Combine demographic data with survey responses to analyze preferences across different age groups.
   - Join website traffic data with user behavior data to analyze user engagement patterns.
   - Merge geographical data with sales data to analyze regional sales performance.
   - Combine inventory data with sales data to analyze stock levels and sales trends.
   - Merge employee data from multiple departments to analyze cross-departmental performance.
   - Combine social media data with customer data to analyze customer sentiment and behavior.

6. Data Transformation - Combining Columns

   - **“Add a column to the table by combining first name and last name, and call that new call full name”**
   - Concatenate first name and last name columns to create a full name column.
   - Combine address columns (street, city, state, zip code) into a single address column.
   - Merge date and time columns to create a single datetime column.
   - Create a new column by combining categorical variables from multiple columns into a single categorical variable.
   - Combine numerical columns representing different aspects of a product to create an aggregated score.
   - Concatenate text columns containing different parts of an article to create a full text column.
   - Combine numerical columns representing different time intervals to create a total duration column.
   - Merge multiple columns containing Boolean values to create a single Boolean column indicating overall status.
   - Combine multiple columns containing ratings or scores to compute an average rating or score.

- Concatenate country code and phone number columns to create a complete phone number column.

## 7. (H) Data Transformation - Spreading a column into multiple (for groups)

Spreading a column into multiple columns, often referred to as "pivoting" or "reshaping" data, is a common data manipulation technique.

- **"Split the name column into 2 columns for first name and last name"**
- **"Split the order date column into separate columns for year, month, and day"**
- Transform a single column of dates into separate columns for year, month, and day.
- Pivot a categorical column to create binary indicator columns for each category.
- Spread a column containing quarterly sales data into separate columns for each quarter.
- Convert a column with comma-separated values into multiple binary indicator columns.
- Pivot a column containing responses to a survey question into separate columns for each response option.
- Spread a column with time-series data into multiple columns representing different time intervals (e.g., hourly, daily, weekly).
- Transform a column containing hierarchical data (e.g., JSON or XML) into multiple columns.
- Spread a column containing multiple attributes or features into separate columns for each attribute.
- Pivot a column containing sales data by product category to create separate columns for each product category.
- Transform a column with nested lists or arrays into multiple columns representing each element in the list or array.

## 8 . (EZ) Descriptive Analysis: Simple implicit metric calculation

Simple explicit metric calculations are essential for understanding and analyzing datasets effectively

- **Given the dataset "car_info_02.csv", determine the average acceleration of all vehicles whose country of origin is usa.**
- Calculate the total sum of sales revenue for a specific time period.
- Determine the average price of products in the dataset.
- Compute the total number of transactions recorded in the dataset.
- Calculate the maximum value of a numerical attribute (e.g., maximum temperature, maximum sales volume).
- Determine the minimum value of a numerical attribute (e.g., minimum inventory level, minimum price).
- Compute the percentage of missing values in a specific column.
- Calculate the median value of a numerical attribute (e.g., median income, median response time).
- Determine the standard deviation of a numerical attribute (e.g., standard deviation of customer age, standard deviation of product weight).
- Calculate the proportion of records meeting certain criteria (e.g., proportion of customers who made repeat purchases, proportion of products with high ratings).
- Compute the rate of change over time for a specific metric (e.g., monthly sales growth rate, quarterly customer acquisition rate).

## 9. (H) Descriptive Analysis: Simple implicit metric calculation

Customer Satisfaction Score: Based on feedback or ratings provided by customers.\

Product Popularity Index: Determined by the frequency of purchases or views.
Customer Loyalty Score: Derived from the frequency and value of repeat purchases.\

Employee Engagement Level: Inferred from responses to surveys or performance metrics.\

User Engagement Rate: Based on metrics like time spent on a website or app.\

Customer Lifetime Value (CLV): Estimated based on historical purchase behavior and retention rates.\

Brand Awareness Level: Indicated by metrics such as social media mentions or brand recognition surveys.\

Market Share: Calculated by comparing a company's sales to the total market sales.\

Conversion Rate: Calculated by dividing the number of conversions by the total number of visitors or leads.\

Churn Rate: Determined by the percentage of customers who stop using a product or service over time.

These questions aim to uncover insights from implicit metrics that can inform strategic decision-making and business optimization efforts.

- What factors contribute to fluctuations in customer satisfaction scores over time?
- How does user engagement correlate with product feature updates or changes?
- What impact does employee engagement have on productivity and overall company performance?
- How does brand awareness vary across different demographic segments?
  What strategies can be implemented to increase customer loyalty and retention rates?
- What channels or campaigns are most effective in improving brand perception and recognition?
- What are the primary drivers of market share growth or decline within a specific industry?
- How does the conversion rate differ across various marketing channels or sales funnels?
- What factors contribute to customer churn, and how can they be mitigated or addressed?
- What patterns emerge in user behavior prior to and following product updates or releases?

## 10. (H) Descriptive Analysis: Complex metric calculation

These complex metric calculations require advanced analytical techniques, including machine learning, statistical modeling, and predictive analytics, to derive meaningful insights and drive business decisions.

Customer Lifetime Value (CLV) Prediction: Using historical purchase data, predict the future value of individual customers over their lifetime.\

Market Basket Analysis: Identify associations between products frequently purchased together to optimize product placement and promotions.\

Customer Segmentation: Cluster customers based on various attributes such as demographics, purchase behavior, and engagement level.\

Sales Forecasting: Develop models to forecast future sales based on historical trends, seasonality, and external factors.\

Product Cohort Analysis: Analyze the behavior of groups of customers who signed up for a product or service during the same time period.\

Customer Churn Prediction: Predict which customers are likely to churn based on their historical interactions and behavior.\

Dynamic Pricing Models: Develop pricing strategies based on demand elasticity, competitor pricing, and customer segments.\

Marketing Attribution Modeling: Determine the impact and effectiveness of various marketing channels on customer conversions.\

Risk Assessment and Fraud Detection: Develop algorithms to identify potential fraud or anomalies in financial transactions or user behavior.\

Customer Lifetime Value Optimization: Develop strategies to maximize CLV through targeted marketing, retention efforts, and personalized experiences.

- How can we leverage machine learning algorithms to predict customer churn and develop proactive retention strategies?
- What are the key drivers influencing customer lifetime value, and how can we optimize marketing spend to maximize CLV?
- What clustering algorithms can we use to segment customers based on their purchase behavior, demographics, and psychographic attributes?
- How can we apply time series forecasting techniques to predict demand and optimize inventory management?
- What are the most effective strategies for dynamic pricing in e-commerce, considering factors like demand elasticity and competitor pricing?
- What machine learning models can be employed to detect and prevent fraudulent activities in financial transactions or user accounts?
- How can we attribute conversions to different marketing touchpoints along the customer journey using multi-touch attribution models?
- What predictive modeling techniques can help us anticipate changes in customer preferences and adapt our product offerings accordingly?
- What approaches can we take to optimize the effectiveness of recommendation systems by personalizing recommendations based on user behavior and preferences?
- How can we perform A/B testing and experiment design to evaluate the impact of new features, marketing campaigns, or pricing strategies on key metrics such as conversion rates and revenue?

## 11. (M) Descriptive Analysis: Multiple simple/complex calculations in the same query

- **Using the attached CSV file containing song data. First, calculate the average beats per minute (BPM) for songs in each year from 2000 to 2005. Next, compute the year-over-year percentage change in the average BPM, identifying the year with the highest increase and the year with the highest decrease. For the year with the highest increase, find the song with the highest BPM, and for the year with the highest decrease, find the song with the lowest BPM.**
- Calculate the total revenue, average order value, and number of orders placed by each customer.
- Determine the percentage of total sales contributed by each product category, along with the average sales price and total quantity sold for each category.
- Compute the average time spent on a website per session, the number of pages visited per session, and the bounce rate for each user segment.
- Identify the top-performing sales regions based on total sales revenue, average order value, and customer acquisition cost.
- Calculate the correlation between customer satisfaction scores, employee engagement levels, and sales performance metrics.
- Estimate the customer lifetime value (CLV) for different customer segments based on historical purchase data and retention rates.
- Determine the effectiveness of marketing campaigns by analyzing conversion rates, click-through rates, and return on investment (ROI) for each campaign.
- Perform cohort analysis to examine customer retention rates over time, average order values, and frequency of purchases for different cohorts.
- Compute the weighted average of product ratings based on the number of reviews and the credibility of the reviewers.
- Identify trends in website traffic by analyzing the growth rate, seasonality, and sources of traffic (organic, paid, referral) over time.

# 12. Descriptive Analysis: Visualization - Explicit chart plotting (2-dimensions: line, bar, pie)

These questions help visualize various aspects of the dataset, making it easier to identify trends, patterns, and insights for analysis and decision-making.

- **Create a stacked bar chart representing the distribution of 'cylinders' within each 'origin'. I have attached the dataset. Please provide me with the code.**
- **Based on the file exam_score_03.csv, I want you to plot in a 3D Scatter plot of the exams scores for female students, plotting the data with different colours and markers according to the weekly hours of study. Set the size of the plot as 12x12. Make sure that all the axis labels are shown correctly, adding an additional padding if necessary**
- **“Create a pie chart showing marketing spend by channel”**
- Plot a line chart showing the trend of sales revenue over time (e.g., monthly or quarterly sales).
- Create a bar chart comparing the sales performance of different product categories in terms of total revenue generated.
- Plot a pie chart illustrating the distribution of market share among competing brands or companies.
- Visualize the trend of website traffic over the course of a month using a line chart.
- Compare the distribution of customer ages using a bar chart to identify the predominant age groups.
- Create a pie chart representing the distribution of customer segments based on purchasing behavior (e.g., new customers, repeat customers, loyal customers).
- Plot a line chart to show the fluctuation of stock prices for a specific company over the past year.
- Compare the average ratings of products across different categories using a bar chart.
- Visualize the distribution of employee salaries using a bar chart to identify salary ranges and disparities.
- Create a pie chart illustrating the composition of expenses within a budget (e.g., percentage allocated to rent, utilities, salaries, etc.).

# 13. (H) Descriptive Analysis: Visualization - Complex chart plotting (3+ dimensions: heatmap, bubble)

These complex chart plotting questions allow for the visualization of multidimensional data, enabling analysts to identify patterns, trends, and insights that may not be apparent from simple visualization

- Create a heatmap to visualize the correlation matrix of variables in the dataset, showing the strength and direction of relationships.
- Plot a bubble chart representing the relationship between GDP, population size, and carbon emissions for different countries.
- Visualize the distribution of customer demographics (age, income, and location) using a 3D bubble chart.
- Create a heatmap illustrating the frequency of customer purchases across different product categories and time periods.
- Plot a bubble chart to compare the market share, revenue, and growth rate of companies within a specific industry.
- Visualize the relationship between temperature, humidity, and rainfall using a 3D scatter plot for different geographic regions.
- Create a heatmap to visualize the sentiment analysis results of customer reviews for different products or services.
- Plot a bubble chart representing the relationship between education level, income, and job satisfaction among employees in various industries.
- Visualize the distribution of crime rates across different neighborhoods using a heatmap overlaid on a map of the city.
- Create a bubble chart to compare the performance of stocks in a portfolio based on returns, volatility, and market capitalization.

## 14. General Data Exploration: Pattern Recognition or generic insight

- **“Identify patterns, outlier and anomalies in the data”**
- **"Identify any significant trends or patterns in the sales data."**
- **“Show me some insight about the data”**
- **“Tell me something interesting/new about the data”**
- **“What should i focus on in the data‘**
- What is the distribution of numerical variables in the dataset, and are there any outliers?
- Are there any correlations between numerical variables, and if so, what is the strength and direction of these relationships?
- What are the most common values and frequencies for categorical variables in the dataset?
- How does the distribution of a target variable vary across different categories or segments in the dataset?
- Are there any missing values in the dataset, and if so, what is the extent and pattern of missingness?
- What are the summary statistics (mean, median, standard deviation) for numerical variables, and how do they compare across different groups?
- Are there any temporal trends or seasonality patterns present in the data, and how do they vary over time?
- What are the most frequent words or phrases in text data, and do they reveal any underlying themes or topics?
- How do distributions of variables differ between different subgroups or clusters identified within the dataset?
- Are there any anomalies or unexpected patterns in the data that warrant further investigation or explanation?

## 15. (H) Specific Data Explorations: Insights about X

These questions can help uncover insights specific to the variable of interest and provide valuable information for further analysis and decision-making.

- What are the top five most common categories/values for variable X, and what proportion of the dataset do they represent?
- How does the distribution of variable X vary across different groups or categories within the dataset?
- What is the average/median value of variable X, and how does it change over time, if applicable?
- Are there any notable correlations or relationships between variable X and other variables in the dataset?
- What is the trend of variable X over time, and are there any seasonal patterns or fluctuations?
- How does the distribution of variable X differ between different demographic segments or customer groups, if applicable?
- Are there any outliers or anomalies in the values of variable X, and if so, what might explain them?
- What is the geographical distribution or spatial pattern of variable X, if applicable?
- How does the sentiment or sentiment polarity of textual data relate to the values of variable X, if applicable?
- What factors or variables are most strongly associated with high or low values of variable X, based on regression analysis or feature importance measures?

## 19. (H) Advanced analysis

- Cohort Analysis: How does customer retention vary over time for different cohorts, and what factors contribute to differences in retention rates?

- Time Series Forecasting: Can we accurately forecast future sales or demand based on historical patterns and external factors, and how confident are we in these predictions?

- Customer Segmentation: What distinct segments or clusters exist within our customer base, and how do they differ in terms of demographics, behaviors, and preferences?

- Text Mining and Sentiment Analysis: What are customers saying about our products or services on social media or review platforms, and what sentiment trends can we identify over time?

- Predictive Modeling: Can we build a predictive model to anticipate customer churn, and which variables are the most influential in predicting churn behavior?

- Market Basket Analysis: What are the most common product combinations purchased together, and how can we use this information to optimize product placement and promotions?

- Network Analysis: How are individuals or entities connected within a network (e.g., social network, supply chain), and what insights can we derive from analyzing these connections?

- Survival Analysis: What factors influence the survival (or failure) of products or customers over time, and how can we estimate survival probabilities?

- Geospatial Analysis: What spatial patterns or trends exist within our data (e.g., regional sales, distribution of resources), and how can we visualize and interpret these patterns?

- Dynamic Pricing Optimization: How can we dynamically adjust prices in response to changing market conditions and customer behavior, and what impact does this optimization have on revenue and profitability?

- Time Series Analysis: How have sales trends evolved over time, and what seasonal patterns or trends can be identified?

- Predictive Modeling: Can we build a model to forecast future customer behavior, such as purchasing patterns or churn rates?

- Customer Lifetime Value (CLV) Analysis: What is the expected lifetime value of a customer, and how can it be maximized through targeted marketing strategies?

- Market Segmentation Analysis: How can we segment our market based on demographic, psychographic, or behavioral attributes, and tailor our marketing efforts accordingly?

- Customer Journey Analysis: What are the key touchpoints in the customer journey, and how can we optimize each touchpoint to improve customer satisfaction and retention?

- Text Mining and Natural Language Processing (NLP): What insights can be gleaned from analyzing customer feedback, reviews, or social media posts using NLP techniques?

- A/B Testing and Experimentation: How can we design and analyze experiments to evaluate the impact of new features, marketing campaigns, or pricing strategies?

- Prediction and Prevention: What factors contribute to customer churn, and how can we proactively identify and prevent churn through targeted interventions?

- Market Basket Analysis: What products are frequently purchased together, and how can we leverage this information for cross-selling and upselling opportunities?

- Geospatial Analysis: How does geographic location impact customer behavior, and how can we use geospatial analysis to optimize resource allocation and expansion strategies?

# 20. Generating Files - Explicit

- **“Remove duplicate entries in the original data and save it to a new CSV”**
- **Create a table showing the total sales, average order value, and number of orders for each product category and save the table to a tsv file named sales_aggregation.tsv.**
- Generate a CSV file containing summary statistics (mean, median, standard deviation, etc.) for numerical variables in the dataset.
- Create a JSON file that organizes the data into a nested structure based on categorical variables.
- Generate an Excel spreadsheet with separate sheets for different segments or categories within the dataset.
- Create a text file containing descriptive metadata about the dataset, including variable names, data types, and descriptions.
- Generate a CSV file containing cleaned and transformed data after preprocessing steps, such as imputation of missing values or encoding categorical variables.
- Create a JSON file containing aggregated data, such as total sales revenue by month or average customer satisfaction scores by region.
- Generate a PDF report summarizing key insights and findings from the dataset, including visualizations and interpretations.
- Create a SQL script file that contains database table creation statements based on the dataset schema.
- Generate multiple CSV files partitioned by date or category, making it easier to manage and analyze large datasets.
- Create a Markdown file containing the dataset documentation, including information about the source, collection methods, and data cleaning procedures.

## forbidden 🔥

- Bokeh \
  An interactive visualization library that renders plots in browsers.
- Seaborn \
  Statistical data visualization based on matplotlib.
- Plotly \
  An interactive, browser-based, data visualization library.

## lang & libs

Python 3.10. If a library is explicitly requested in the query, then it is limited to this list of approved libraries:

- Matplotlib \
  For generating static plots based on datasets provided.
- Pandas\
  For dataset importing & dataset manipulation.
- Numpy\
  For general computation & matrix manipulations.
- MP Math\
  A library for arbitrary-precision floating-point arithmetic.
- Scipy \
  For advanced computation
- Sympy \
  For Symbolic Algebra.

👉 Study the dataset and familiarize yourself with the data to understand what information it has and start thinking about things you could ask the model given the dataset.

## Examples of non-W questions include:

- Yes/No Questions:\
  Questions that can be answered with a simple "yes" or "no" without the use of interrogative words.

Example: Is it raining outside?

- Choice Questions:\
  Questions that offer options for the respondent to choose from.

Example: Do you prefer tea or coffee?

- How Questions:\
  Questions that begin with the word "how" and seek information about the manner or method of doing something.

Example: How do you bake a cake?

- Tag Questions:\
  Questions added to the end of a statement to confirm or clarify information.

Example: You like ice cream, don't you?
-Alternative Questions: Questions that present two or more alternatives for the respondent to choose from.

Example: Would you like pizza or pasta for dinner?
