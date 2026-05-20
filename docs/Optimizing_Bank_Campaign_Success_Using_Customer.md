# Optimizing Bank Campaign Success Using Customer & Economic Insights

## Authors

**Yara Ibrahim Alzubaidi**  
ID: 202211200

**Supervised by**  
Dr Husam Barham

**Course:** 307498 – Graduation Project  
**Semester:** Second Semester, 2026/2027

---

**Contents**

[**Abstract** 3](#_Toc230049292)

[**Acknowledgment** 4](#_Toc230049293)

[**Business Intelligence Project Description and Objectives** 5](#_Toc230049294)

[**Project Description and Goal** 5](#_Toc230049295)

[**Project Objectives** 5](#_Toc230049296)

[**Data Research and Acquiring Effort** 6](#_Toc230049297)

[**Data Description and Understanding** 7](#_Toc230049298)

[**Exploratory Data Analysis (EDA)** 9](#_Toc230049299)

[**Data Primary Cleaning and Transformation** 10](#_Toc230049300)

[**Data Visualization and Insights** 11](#_Toc230049301)

[**Dashboard Design & Business Insights** 11](#_Toc230049302)

[**Advanced Analytics and AI Modeling** 22](#_Toc230049303)

[**Prediction Analysis** 23](#_Toc230049304)

[**Logistic Regression** 24](#_Toc230049305)

[**Random Forest** 25](#_Toc230049306)

[**Quantitative Assessment of the Models** 26](#_Toc230049307)

[**Model Comparison** 27](#_Toc230049308)

[**Clustering** 29](#_Toc230049309)

[**Clustering Results Interpretation** 30](#_Toc230049310)

[**Tools Research and Selection Effort** 33](#_Toc230049311)

[**Project Deployment Effort - Use Case** 33](#_Toc230049312)

[**Results** 35](#_Toc230049313)

[**References** 35](#_Toc230049314)

---

## Abstract

This project investigates the application of business intelligence, data analytics, and machine learning techniques to analyze customer behavior and improve the effectiveness of direct marketing campaigns in the banking sector. Using the Bank Marketing dataset, the study aims to support data-driven decision-making by identifying the factors that influence customer subscription to term deposit services.

The implementation phase involved data cleaning, preprocessing, transformation, and exploratory data analysis using Python and Google Colab. Interactive dashboards were developed in Power BI to visualize customer distribution, campaign performance, response rates, and relationships between customer attributes and subscription outcomes. Predictive analytics was conducted using Logistic Regression and Random Forest classification models to predict whether a customer would subscribe to a term deposit campaign.

Model performance was evaluated using classification metrics including accuracy, precision, recall, F1-score, ROC Curve, and AUC Score. In addition, K-Means clustering was applied to segment customers into distinct groups based on financial and behavioral characteristics.

**Key Results:** The Random Forest model outperformed Logistic Regression by capturing more complex relationships between variables. Analysis revealed that call duration, previous campaign outcome, campaign contacts, balance level, and economic indicators were among the most influential factors affecting customer responses. Customer clustering identified meaningful segments enabling more targeted marketing strategies.

Overall, the integration of descriptive analytics, predictive modeling, clustering, and business intelligence dashboards within a unified framework proved effective in delivering actionable insights, improving customer targeting, optimizing marketing campaign efficiency, and supporting strategic decision-making in the banking industry.

---

## Acknowledgment

I would like to express my sincere gratitude to my professor and academic supervisor for their invaluable guidance, continuous support, and constructive feedback throughout the development of this project. Their expertise, encouragement, and dedication played a significant role in enhancing both the quality of this work and my academic growth in the field of Business Intelligence and Data Analytics.

I would also like to extend my deepest appreciation to my family and friends for their constant encouragement, patience, and motivation during every stage of this journey. Their support gave me the strength and determination to overcome challenges and successfully complete this project.

Special thanks are also extended to the faculty and staff members whose commitment to academic excellence created a supportive learning environment that encouraged innovation, critical thinking, and exploration. Their assistance and guidance were instrumental in the successful completion of this project.

Finally, I am grateful to everyone who contributed directly or indirectly to this work. Your support and encouragement have had a meaningful impact on both my academic and personal development.

---

## Business Intelligence Project Description and Objectives

### Project Description and Goal

This project focuses on applying Business Intelligence, data analytics, and machine learning techniques within the banking sector to analyze direct marketing campaigns and improve customer targeting strategies. Using the Bank Marketing dataset, the project aims to transform raw customer and campaign data into meaningful insights through descriptive analytics, predictive modeling, and customer segmentation techniques.

The project analyzes customer demographics, financial information, campaign interactions, and economic indicators to better understand the factors that influence customer subscription to bank term deposit services. By integrating tools such as Python, Google Colab, and Power BI, the project demonstrates how data-driven approaches can support financial institutions in improving marketing effectiveness, enhancing customer targeting, reducing operational costs, and supporting strategic decision-making.

Interactive dashboards, predictive machine learning models, and clustering techniques were implemented to provide both analytical insights and intelligent decision-support solutions for marketing campaign optimization.

### Project Objectives

#### 1. Analyze Customer and Campaign Performance

Examine historical banking marketing data to identify trends, behavioral patterns, and factors affecting customer subscription outcomes. The analysis focuses on customer demographics, financial characteristics, campaign communication methods, and economic indicators using descriptive analytics and visualization techniques.

#### 2. Predict Customer Subscription Response

Develop and evaluate supervised machine learning classification models, including Logistic Regression and Random Forest, to predict whether a customer will subscribe to a bank term deposit campaign based on customer and campaign-related features.

#### 3. Identify Key Factors Influencing Campaign Success

Determine the most influential variables affecting customer responses and campaign performance, such as:
- Call duration
- Previous campaign outcomes
- Contact frequency
- Balance levels
- Job type
- Age
- Economic indicators
- Loan and housing status

Feature importance analysis was performed to understand which attributes contribute most significantly to successful marketing outcomes.

#### 4. Segment Customers Using Clustering

Apply unsupervised learning techniques, specifically K-Means clustering, to group customers according to their financial behavior, campaign interaction patterns, and response tendencies. The clustering process helps identify high-potential customer groups and supports personalized marketing strategies.

#### 5. Enhance Decision-Making Through Business Intelligence

Design interactive Power BI dashboards that visualize key performance indicators (KPIs), campaign trends, customer behavior patterns, and predictive insights. These dashboards support faster, more effective, and data-driven managerial decision-making within banking marketing operations.

---

## Data Research and Acquiring Effort

The data used in this project was obtained from the publicly available Bank Marketing dataset, which contains real-world direct marketing campaign data collected from a Portuguese banking institution. The primary objective during the data acquisition phase was to obtain a dataset that accurately represents customer demographics, financial characteristics, marketing campaign interactions, and customer responses to bank term deposit offers.

The selected dataset contains detailed information about customers, including:
- Age, job type, marital status, education level
- Balance information, loan status
- Communication methods
- Previous campaign interactions
- Economic indicators (employment variation rate, consumer price index, consumer confidence index)
- Target variable indicating term deposit subscription

This dataset was chosen because it provides comprehensive information required for descriptive analytics, predictive modeling, customer segmentation, and business intelligence dashboard development.

The dataset was obtained from the UCI Machine Learning Repository and imported into Python, Google Colab, Microsoft Excel, and Power BI for data cleaning, preprocessing, transformation, visualization, and machine learning implementation. Since the dataset is publicly available and widely used in banking analytics and machine learning research, it provides a reliable foundation for applying business intelligence and predictive analytics techniques.

The selection of this dataset enabled a comprehensive analysis of customer behavior and campaign performance by combining descriptive analytics, predictive modeling, and clustering techniques. This supports the development of data-driven marketing strategies that can help financial institutions improve customer targeting, increase campaign response rates, optimize communication strategies, and reduce unnecessary marketing costs.

---

## Data Description and Understanding

### Data Dictionary

The dataset used in this project contains customer demographic information, financial attributes, marketing campaign details, and economic indicators related to direct bank marketing campaigns.

![Descriptive Alt Text](..\images\1.png)

| Column Name | Description | Type | Use |
|---|---|---|---|
| age | Age of the customer | Numerical | Used to analyze customer demographics, age group behavior, and response patterns |
| job | Type of customer occupation | Categorical | Helps identify which professions respond more positively to campaigns |
| marital | Customer marital status | Categorical | Used for customer segmentation and behavioral analysis |
| education | Education level of the customer | Categorical | Helps analyze relationship between education level and subscription behavior |
| default | Indicates whether the customer has credit in default | Binary/Categorical | Used to evaluate financial risk and customer reliability |
| balance | Average yearly account balance | Numerical | Important financial indicator used in response prediction and customer segmentation |
| housing | Indicates whether the customer has a housing loan | Binary/Categorical | Used to study the impact of financial obligations on customer responses |
| loan | Indicates whether the customer has a personal loan | Binary/Categorical | Helps analyze how existing loans influence subscription behavior |
| contact | Type of communication contact (cellular/telephone) | Categorical | Used to evaluate communication effectiveness |
| month | Last contact month of the year | Categorical/Date | Used for seasonal trend analysis and campaign timing evaluation |
| day_of_week | Last contact day of the week | Categorical/Date | Helps identify the most effective communication days |
| duration | Duration of the last contact call in seconds | Numerical | Strong predictor of customer response and campaign engagement |
| campaign | Number of contacts performed during the current campaign | Numerical | Used to analyze communication frequency and campaign effectiveness |
| pdays | Number of days since the customer was previously contacted | Numerical | Measures customer recency and previous interaction timing |
| previous | Number of contacts performed before the current campaign | Numerical | Helps evaluate historical customer engagement |
| poutcome | Outcome of the previous marketing campaign | Categorical | One of the most important predictors for future campaign success |
| emp.var.rate | Employment variation rate | Numerical | Economic indicator used to analyze employment conditions impact |
| cons.price.idx | Consumer Price Index (CPI) | Numerical | Measures inflation and economic environment |
| cons.conf.idx | Consumer Confidence Index (CCI) | Numerical | Indicates customer confidence and spending behavior |
| euribor3m | Euribor 3-month interest rate | Numerical | Represents market interest rates affecting financial decision-making |
| nr.employed | Number of employees in the economy | Numerical | Economic indicator reflecting labor market conditions |
| y | Customer subscribed to term deposit | Binary/Target | Target variable for predictive modeling |

---

## Exploratory Data Analysis (EDA)

Initial Exploratory Data Analysis was performed to understand the structure, distribution, and behavior of the data before applying predictive and clustering models.

### Data Distribution Analysis

**Histograms and Descriptive Statistics:** Applied to numerical variables such as Sales Amount, Quantity, and Discount. The analysis showed that sales amount follows a right-skewed distribution, indicating that most transactions are low to medium in value, while a small number of transactions contribute to very high sales.

**Box Plots:** For quantity and discount revealed the presence of extreme outliers, particularly in discount values, suggesting occasional large discounts applied to specific transactions.

### Categorical Analysis

**Bar Charts and Pivot Tables:** Used to analyze categorical variables such as Location, Value Category, and Payment Method. The results showed that certain regions contribute more significantly to total sales, while large value category transactions, although fewer, account for a substantial portion of revenue.

### Relationship Analysis

**Scatter Plots:** Between Quantity and Sales Amount indicated a strong positive relationship, confirming that higher quantities generally lead to higher sales values. However, variations caused by discounting behavior justified the need for predictive modeling.

### Key Insights

The EDA phase provided valuable insights into:
- Key business drivers
- Data variability and outliers
- Feature selection for prediction and clustering models
- Patterns affecting customer engagement and campaign success

---

## Data Primary Cleaning and Transformation

Data cleaning and transformation is a critical step in preparing the dataset for analysis, visualization, and machine learning modeling.

![Descriptive Alt Text](..\images\2.png)

### Cleaning Procedures

**Changed Data Types:** Columns were assigned appropriate data types such as numeric, text, and categorical formats to ensure accurate analysis and visualization.

**Removed Duplicate Records:** Duplicate rows were identified and removed to improve data consistency and avoid biased results.

**Removed Blank Rows and Errors:** Blank rows, missing values, and invalid records were filtered and removed to maintain a clean and reliable dataset.

**Trimmed and Standardized Text:** Text columns such as job, education, marital status, and month were cleaned using text trimming to remove extra spaces and formatting inconsistencies.

**Added Conditional Columns:** Conditional columns were created to support customer categorization, segmentation, and business analysis within Power BI dashboards.

**Filtered Irrelevant Data:** Unnecessary and inconsistent records were excluded to keep only meaningful data for analysis and predictive modeling.

### Purpose

These preprocessing steps ensured that the dataset became accurate, consistent, and analysis-ready for exploratory analysis, machine learning models, clustering, and dashboard visualization.

---

## Data Visualization and Insights

### Dashboard Design & Business Insights


![Descriptive Alt Text](..\images\3.png)


#### Overall Dashboard Purpose

The dashboard was developed to analyze customer behavior, financial status, and campaign response patterns using business intelligence and data analytics techniques. It provides interactive visual insights that help businesses understand customer segments, improve marketing strategies, optimize communication efforts, and support data-driven decision-making.

### Dashboard 1: Customer Demographics and Response Analysis

#### Chart 1: Age Group by Customers

**Description:** This chart shows the number of customers within each age group category.

**Insight & Business Use:** Most customers belong to the Midlife Adults and Early Adults groups, while Seniors represent the smallest segment. This helps businesses understand their dominant customer demographics and create age-targeted marketing campaigns.

#### Chart 2: Age Group by Response Rate

**Description:** Displays the campaign response rate across different age groups.

**Insight & Business Use:** Youth customers achieved the highest response rate, indicating they are more likely to respond positively to campaigns. This helps businesses focus marketing efforts on highly responsive customer groups and improves campaign efficiency.

#### Chart 3: Balance Group by Customers

**Description:** Illustrates the distribution of customers based on balance categories such as Low, Medium, High, and Negative.

**Insight & Business Use:** Many customers fall within the Low balance category. This visualization supports customer financial profiling and helps businesses understand the financial structure of their customer base.

#### Chart 4: Balance Group by Response Rate

**Description:** Compares customer response rates according to balance groups and loan status.

**Insight & Business Use:** Customers with High and Medium balances generally showed higher response rates, especially customers without loans. This helps identify financially stable customers with higher campaign potential and supports better customer targeting strategies.

#### Chart 5: Call Duration Impact

**Description:** Shows the relationship between call duration and customer engagement levels.

**Insight & Business Use:** Short and Very Short calls were the most frequent interaction types. The chart helps evaluate communication effectiveness and assists businesses in optimizing call strategies to improve customer engagement and campaign outcomes.

#### Chart 6: Effect of Contact Frequency on Response Rate

**Description:** This line chart demonstrates how customer response rates change according to the number of campaign contacts.

**Insight & Business Use:** The response rate generally decreased as contact frequency increased, indicating that excessive contact may negatively affect customer engagement. This insight helps businesses determine the optimal number of customer interactions and avoid over-contacting customers during campaigns.


![Descriptive Alt Text](..\images\4.png)


#### Post-Call Insight: Duration vs Response Behavior

**Description:** This bubble chart shows the relationship between call duration categories and customer response behavior based on previous campaign outcomes.

**Insight & Business Use:** Customers with previous successful outcomes achieved the highest response rates, especially for Short and Very Short calls. Customers with previous failures showed much lower response rates despite higher frequencies. This suggests that previous campaign success and communication duration strongly influence customer engagement.. Businesses can use these insights to optimize call strategies, target high-potential customers, and improve future campaign performance.

---

![Descriptive Alt Text](..\images\5.png)


#### Chart 1: Job Title by Customers

**Description:** Shows the distribution of customers across different job categories.

**Insight & Business Use:** Administrative and blue-collar jobs represent the largest customer groups, while unemployed and unknown categories are the smallest. This helps businesses understand customer demographics and target dominant occupational segments.

#### Chart 2: Job Title by Response Rate

**Description:** Displays customer response rates according to job category.

**Insight & Business Use:** Students achieved the highest response rates, while unknown and entrepreneur categories had lower rates. This helps businesses focus campaigns on more responsive occupational groups.

#### Chart 3: Education Level by Response Rate

**Description:** Compares campaign response rates across education levels.

**Insight & Business Use:** Customers with high school education showed slightly higher response rates. This supports customer segmentation and helps optimize campaign targeting based on educational background.

#### Chart 4: Default by Response Rate

**Description:** Shows response rates based on customer default status.

**Insight & Business Use:** Customers with previous defaults had the highest response rate. This insight helps evaluate financial behavior patterns and improve risk-based customer targeting.

#### Chart 5: Contact Type by Response Rate

**Description:** Illustrates response rates by communication method (cellular, telephone, unknown).

**Insight & Business Use:** Cellular contact achieved the highest response rate, suggesting mobile communication is more effective for customer engagement and campaign success.

#### Chart 6: Housing by Response Rate

**Description:** Compares response rates according to housing loan status.

**Insight & Business Use:** Response rates were relatively similar across categories, with customers having housing loans showing slightly higher engagement. This helps assess the influence of financial commitments on campaign responses.

---

![Descriptive Alt Text](..\images\6.png)


#### Chart 1: Response Rate by Contact Recency and Previous Campaign Outcome

**Description:** This chart analyzes responses based on the timing of previous contacts and prior campaign results. Recently contacted customers show higher success rates, while customers never contacted or with failed outcomes have lower engagement.

**Business Use:** Helps optimize contact timing and improve campaign planning by focusing on customers with higher response potential.

#### Chart 2: Campaign Response by Marital Status

**Description:** This chart compares campaign responses across marital groups. Married customers represent the largest customer segment and contribute the highest number of responses.

**Business Use:** Supports customer segmentation and enables targeted campaigns based on demographic characteristics.

#### Chart 3: Loan by Response Rate

**Description:** This chart evaluates customer responses according to loan status.

**Business Use:** Helps understand how financial obligations may influence customer behavior and campaign effectiveness.

---

![Descriptive Alt Text](..\images\7.png)

#### Dashboard Purpose

This dashboard presents deeper analytical insights into customer behavior and campaign performance using grouped statistical tables. It helps identify how factors such as job type, age group, month, contact method, previous campaign outcome, and balance level influence customer responses and success rates.

#### Analysis Tables

**1. Job vs Age Group Table**
Response rates across different job categories and age groups. Youth and students show relatively higher response values compared to other segments.

**Business Use:** Helps businesses identify which customer demographics are more responsive to campaigns, allowing better targeting and personalized marketing strategies.

**2. Month vs Age Group Table**
Analyzes customer response behavior across months and age categories. Months such as October, December, and September show stronger performance.

**Business Use:** Supports seasonal analysis and helps determine the best periods to launch campaigns for higher effectiveness.

**3. Job vs Contact Type Table**
Compares customer responses based on communication methods across job categories. Cellular communication generally shows stronger results.

**Business Use:** Helps organizations choose the most effective communication channels for different customer segments.

**4. Previous Outcome vs Contact Frequency Table**
Shows how previous campaign outcomes relate to the number of customer contacts. Customers with previous successful outcomes demonstrate significantly higher response values.

**Business Use:** Assists businesses in prioritizing customers with positive historical interactions and optimizing follow-up strategies.

**5. Balance Group Analysis Table**
Examines customer responses according to account balance categories. Medium and high balance groups generally show better engagement levels.

**Business Use:** Supports customer value segmentation and helps organizations focus on high-potential customers for sales and retention strategies.

---

![Descriptive Alt Text](..\images\8.png)

#### Dashboard Purpose

This dashboard provides a comprehensive analysis of marketing campaign performance and customer response behavior. It combines KPIs, response trends, economic indicators, and campaign outcomes.

#### Key Components

**1. KPI Cards**
The top KPI cards summarize overall campaign performance, including total customers, responders, response rate, average call duration, and average customer balance.

**Business Use:** Provides a quick overview of campaign effectiveness and customer engagement levels for management monitoring.

**2. Campaign Response %**
This donut chart compares customers who responded "yes" and "no" to the campaign.

**Business Use:** Helps evaluate overall campaign conversion performance and customer acceptance rates.

**3. CPI vs Response Behavior**
This bubble chart analyzes the relationship between economic indicators (CPI) and customer responses.

**Business Use:** Shows how economic conditions may influence customer decisions and campaign outcomes.

**4. Impact of Call Duration and Previous Campaign Outcome**
This stacked column chart examines how previous campaign results and contact duration affect response rates.

**Business Use:** Helps identify the most effective communication duration and customer groups with higher success potential.

**5. Confidence vs Response Trend**
This line chart tracks response trends over time and confidence-related measures.

**Business Use:** Supports trend analysis and helps detect fluctuations in customer engagement behavior.

**6. Campaign Conversion Funnel**
This funnel visual shows the conversion process from total customers to actual responders.

**Business Use:** Measures campaign efficiency and identifies drop-off points in customer conversion.

**7. Month vs Economic Indicators**
This line chart compares monthly trends between economic indicators such as CPI and CCI.

**Business Use:** Helps businesses understand how market and economic conditions impact customer behavior across different periods.

**8. Previous Outcome by Response Rate**
This chart analyzes response rates based on outcomes from previous campaigns.

**Business Use:** Assists in prioritizing customers with positive historical interactions for future campaigns.

**9. Filters and Slicers**
The dashboard includes filters for campaign response, month, contact type, balance group, age group, job category, and previous outcomes.

**Business Use:** Allows interactive analysis and deeper exploration of customer segments and campaign performance.

---

## Advanced Analytics and AI Modeling

This phase of the project focused on applying machine learning and advanced analytics techniques to analyze customer campaign behavior and predict customer responses.

### Supervised Models

To predict whether a customer will respond positively to a marketing campaign, two supervised machine learning models were implemented:

#### Logistic Regression

Logistic Regression was selected as a baseline classification model because of its simplicity, interpretability, and effectiveness in binary classification problems. It helps explain how variables such as balance, duration, age group, contact type, and previous campaign outcome influence customer response behavior.

#### Random Forest

Random Forest was selected because it provides stronger predictive performance and can capture complex and non-linear relationships between customer attributes and campaign responses. It combines multiple decision trees to improve prediction accuracy and reduce overfitting.

---

### Prediction Analysis

Prediction analysis is a machine learning technique used to forecast future outcomes using historical customer and campaign data.

![Descriptive Alt Text](..\images\9.png)


#### Preparing the Prediction Model

The following preprocessing and preparation steps were performed:

- **Retrieve Dataset:** Loads the campaign dataset.
- **Define Target Column:** Sets the response variable (yes/no).
- **Data Splitting:** Divides the data into training and testing sets.
- **Nominal to Numerical:** Converts categorical variables into numerical form.
- **Feature Selection:** Keeps only relevant attributes for prediction.
- **Model Validation:** Evaluates prediction accuracy using classification metrics.

These steps ensured that the dataset was clean, structured, and suitable for machine learning analysis.

---

### Logistic Regression Model

Logistic Regression is a classification algorithm used to predict binary outcomes such as whether a customer will respond to a campaign.
In this project, the model predicts customer response based on variables such as:
Call duration, Balance, Contact type, Previous campaign outcome, Age group, Job category etc..

![Descriptive Alt Text](..\images\10.png)


#### Training Phase

The Logistic Regression model learns patterns and relationships between customer characteristics and campaign responses using the training dataset.

#### Testing Phase

The trained model is applied to unseen data, and its performance is evaluated using classification metrics such as precision, recall, F1-score, and accuracy.

#### Model Performance

The model achieved strong classification performance in identifying customer responses. It successfully distinguished between customers who were likely to respond positively and negatively to the campaign.

#### Overall Interpretation

Logistic Regression provided clear and interpretable insights into how customer and campaign variables affect response behavior. It served as an effective baseline model for campaign prediction and customer analysis.

---

### Random Forest Model

Random Forest is an ensemble machine learning algorithm that builds multiple decision trees and combines their predictions to improve accuracy and stability.
In this project, Random Forest was used to predict customer responses using variables such as: Duration, Balance, Month, Previous campaign outcome, Contact type, Economic indicators etc…

![Descriptive Alt Text](..\images\Picture1.png)


#### Training Phase

The Random Forest model was trained using multiple decision trees generated from random subsets of the training data.

#### Testing Phase

The trained model predicted customer responses on the test dataset, and the results were evaluated using classification performance metrics.

#### Model Performance

The Random Forest model achieved strong classification performance in predicting customer campaign responses. It successfully distinguished between customers who were likely to respond positively and those who were unlikely to respond to the campaign. The model demonstrated high accuracy and reliability by capturing complex patterns and relationships within the customer and campaign data.

This indicates that customer interaction duration and previous campaign success play major roles in predicting responses.

#### Overall Interpretation

Random Forest outperformed Logistic Regression by capturing more complex behavioral patterns and providing higher predictive accuracy. The model proved highly effective for campaign response prediction and customer targeting.

---

### Quantitative Assessment of the Models

Two classification models were evaluated in this project: Logistic Regression and Random Forest. Their performance was compared using accuracy, precision, recall, and F1-score.

| Metric | Logistic Regression | Random Forest |
|---|---|---|
| Accuracy | **74.4%** | **89.9%** |
| Precision (Class 1) | **0.24** | **0.65** |
| Recall (Class 1) | **0.61** | **0.14** |
| F1-Score (Class 1) | **0.34** | **0.23** |
| Weighted F1-Score | **0.79** | **0.87** |

#### Logistic Regression Results

The Logistic Regression model achieved an accuracy of 74.4%. It was able to classify customer responses reasonably well and provided interpretable relationships between customer variables and campaign outcomes.

- Correctly predicted many customer responses.
- Achieved higher recall for positive responses (0.61), meaning it detected more customers likely to respond positively.
- However, precision for positive responses was low (0.24), indicating many false positives.

#### Random Forest Results

The Random Forest model achieved a significantly higher accuracy of 89.9%, outperforming Logistic Regression in overall classification performance.

- Produced much stronger overall prediction accuracy.
- Achieved higher precision (0.65), meaning positive predictions were more reliable.
- Generated a higher weighted F1-score (0.87), indicating better balanced overall performance.
- Reduced misclassification errors significantly.

#### Model Comparison

Comparing the two models quantitatively:

- Random Forest improved accuracy from 74.4% to 89.9%.
- Precision increased from 0.24 to 0.65, meaning Random Forest made more trustworthy positive predictions.
- Weighted F1-score improved from 0.79 to 0.87, showing stronger overall classification quality.
- Logistic Regression had better recall for positive cases (0.61 vs 0.14), meaning it captured more positive responses, but at the cost of many false alarms.

#### Selected Model: Random Forest

The Random Forest model was selected as the best model for this project because it achieved:

- Higher overall accuracy
- Better precision
- Stronger weighted F1-score
- Lower classification errors
- More stable and reliable predictions

Random Forest also handles complex and non-linear relationships between variables more effectively than Logistic Regression, making it more suitable for real-world customer behavior prediction.

---

### Feature Importance Analysis (Random Forest)

The feature importance chart shows the variables that had the strongest influence on predicting customer responses.

![Descriptive Alt Text](..\images\11.png)


#### Most Important Features

- **Balance (~0.08):** Customers with higher account balances had a stronger impact on campaign response prediction.
- **Duration (~0.07):** Call duration was one of the most influential variables. Longer interactions were strongly associated with positive responses.
- **Day (~0.07):** The day of contact affected campaign success, indicating timing influences customer behavior.
- **Age (~0.06):** Customer age contributed significantly to predicting responses.
- **Month Number (~0.035):** Certain months produced better campaign outcomes than others.

#### Other Important Variables

- Campaign
- Previous Outcome Success
- Pdays
- Consumer Price Index
- Consumer Confidence Index

These variables also contributed to prediction performance but with lower importance scores.

#### Overall Interpretation

The feature importance analysis shows that customer financial condition, communication duration, timing, and demographic characteristics are key drivers of campaign success. These insights help the business improve targeting strategies, optimize campaign timing, and focus on customers with higher response potential.

---

## Clustering

### Overview

Clustering is an unsupervised machine learning technique used to group customers with similar behavioral characteristics without predefined labels.
In this project, clustering was used to identify customer segments based on:
Age group, Job category, Balance group, Contact behavior, Previous campaign outcomes and Response patterns

![Descriptive Alt Text](..\images\12.png)
![Descriptive Alt Text](..\images\Picture2.png)



### Clustering Process Explanation

The clustering process included the following steps:

1. Select Relevant Attributes
2. Convert Nominal Variables to Numerical
3. Normalize Data
4. Detect and Remove Outliers
5. Apply K-Means Clustering
6. Visualize Cluster Results

These steps helped identify meaningful customer segments and hidden behavioral patterns.

---

### Clustering Results Interpretation

The clustering analysis revealed clear differences between customer groups based on age, balance, campaign activity, previous contact history, and economic indicators.

![Descriptive Alt Text](..\images\13.png)


#### Cluster 0 – Standard Customers (Largest Group)

- **Size:** 20,945 records
- **Characteristics:**
  - Average balance and campaign activity
  - Very low previous campaign interaction
  - Positive employment variation rate

**Business Use:** These customers represent the regular customer base with stable but moderate campaign engagement.

#### Cluster 1 – Previously Contacted Customers

- **Size:** 7,268 records
- **Characteristics:**
  - Highest balance among all clusters
  - Extremely high previous contact days (pdays)
  - Moderate previous campaign interactions
  - Lower employment variation rate

**Business Use:** This cluster represents customers who were contacted frequently in previous campaigns and showed moderate engagement behavior.

#### Cluster 2 – High-Engagement Customers

- **Size:** 12,970 records
- **Characteristics:**
  - Highest previous campaign interactions
  - Lower employment variation rate
  - Lower consumer confidence values
  - Stable balance and age characteristics

**Business Use:** These customers demonstrate stronger interaction history and higher engagement potential compared to other groups.

---

### Cluster Comparison and Business Insights

The cluster analysis highlighted differences between customer groups across:

- Account balance
- Campaign frequency
- Previous customer interactions
- Economic conditions
- Customer engagement behavior

#### Key Insights

- Customers with previous campaign interactions are more likely to engage again.
- Higher account balances are associated with better campaign response behavior.
- Frequent previous contact improves customer familiarity and engagement.
- Economic indicators such as employment variation and consumer confidence influence customer behavior.

#### How Clustering Helps the Business

Clustering helps the business better understand customer segments and improve campaign targeting strategies.

**Business Benefits:**

- Identify high-potential customer groups
- Improve campaign targeting efficiency
- Reduce unnecessary marketing costs
- Increase customer engagement rates
- Support personalized marketing strategies

By grouping customers based on similar behavioral and financial characteristics, the company can optimize campaign planning and improve overall marketing performance.

---

## Tools Research and Selection Effort

### Python

Python was used for data preprocessing, machine learning modeling, evaluation, and visualization. Libraries such as Pandas, Scikit-learn, Matplotlib, and NumPy supported the analytical process.

### Power BI

Power BI was used to create interactive dashboards, KPIs, filters, and business visualizations that support decision-making.

### Microsoft Excel

Excel was used during the early stages of data cleaning, inspection, and exploratory analysis.

### Integration

Together, these tools created a complete analytics workflow from data preparation to predictive modeling and visualization.

---

## Project Deployment Effort – Use Case

### 1. Dashboard Monitoring and Decision Support

The Power BI dashboards allow management to monitor:

- Campaign response rates
- Customer behavior
- Conversion funnels
- Response trends
- Economic indicator impacts

Managers can quickly identify successful campaigns, customer segments, and underperforming areas.

### 2. Prediction Models – Campaign Forecasting

The prediction models help forecast customer responses before launching campaigns.

**Business Uses:**

- Identify customers likely to respond positively
- Improve campaign targeting
- Reduce unnecessary marketing costs
- Increase campaign efficiency and ROI

Random Forest provides stronger prediction accuracy, while Logistic Regression provides better interpretability.

### 3. Customer Segmentation – Clustering

Customer segmentation helps classify customers into groups based on behavior and engagement.

**Business Applications:**

- Prioritize high-response customers
- Design personalized campaigns
- Improve customer retention
- Optimize communication strategies

---

### Overall Business Value

By combining dashboards, prediction models, and clustering:

- **Dashboards answer:** "What is happening?"
- **Prediction models answer:** "What is likely to happen next?"
- **Clustering answers:** "Which customer groups should we focus on?"

Together, these analytical approaches improve marketing decisions, customer targeting, campaign efficiency, and overall business performance.

---

## Results

The results demonstrate that combining descriptive analytics, predictive modeling, and clustering provides valuable insights into customer campaign behavior.

### Key Findings

The dashboards revealed that campaign responses are highly influenced by:

- Previous campaign success
- Call duration
- Contact type
- Balance level
- Time period

### Predictive Model Performance

The predictive models successfully forecasted customer responses with strong accuracy, especially the Random Forest model, which captured complex behavioral relationships more effectively.

### Customer Segmentation Outcomes

The clustering analysis identified meaningful customer segments, including:

- High-response customers
- Low-engagement customers
- Balance-based customer groups

These insights help the business focus marketing efforts more efficiently and improve campaign success rates.

### Overall Impact

The project demonstrates how Business Intelligence and AI techniques can transform raw customer data into actionable insights that support smarter marketing strategies and data-driven decision-making.

---

## Conclusion

This graduation project successfully demonstrated the effective integration of Business Intelligence, data analytics, and machine learning techniques in the banking sector. By combining descriptive analytics dashboards, predictive classification models, and unsupervised customer clustering, the project delivered comprehensive insights that can significantly improve marketing campaign effectiveness and customer targeting strategies.

The Random Forest model's superior performance (89.9% accuracy) over the baseline Logistic Regression model proves that capturing complex relationships in customer behavior is crucial for campaign success. The clustering analysis provided actionable customer segments that enable personalized and targeted marketing approaches.

Financial institutions can leverage these insights and methodologies to optimize marketing investments, reduce unnecessary contact efforts, and focus resources on high-potential customer groups, ultimately improving campaign ROI and customer satisfaction.
