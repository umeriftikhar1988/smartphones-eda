Exploratory Data Analysis Report - Smartphone Dataset

This report summarizes the steps taken to perform exploratory data analysis (EDA) on a smartphone dataset containing specifications and prices of 1,020 phones. The goal was to understand the structure, clean the data, extract meaningful features, and identify key patterns in pricing and specifications.

🔹 Step 1: Load and Preview Data
The dataset was loaded using pandas from a CSV file stored on Google Drive. Initial checks showed all columns were stored as strings, including price and specifications. 

🔹 Step 2: Data Overview and Missing Values
The dataset contains 10 columns. We used `df.info()` and `df.isnull().sum()` to examine data types and missing values. Missing values were found in 'camera', 'card', and 'os'.

 🔹 Step 3: Data Cleaning
We cleaned the 'Price' column by removing 'Rs.' and commas, then converted it to an integer. 'camera' and 'card' were filled with 'Unknown'. Rows with missing 'os' values were dropped.

 🔹 Step 4: Feature Engineering
We extracted numerical values from textual columns to create structured features:
- RAM_GB and Storage_GB from 'ram'
- Battery_mAh and Charging_W from 'battery'
  
 🔹 Step 5: Visualization and Patterns
Various plots were used to explore distributions and relationships:
- Histogram of Price
- Countplot of RAM sizes
- OS version distribution
- Correlation heatmap of numeric features
- Boxplots and scatterplots for price vs RAM, battery, and charging
  
🔹 Step 6: Summary and Key Insights
• Smartphones with higher RAM and Storage generally cost more.
• Battery capacity and fast charging are weakly correlated with price.
• Android v12 and v13 dominate the OS distribution.
• Extracted features are now ready for further ML tasks such as price prediction or clustering.

