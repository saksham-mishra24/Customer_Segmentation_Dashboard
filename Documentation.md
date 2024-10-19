# 🌟 **Customer Segmentation & Targeting - Documentation**🌟

## **Project Objective** 🎯
The primary goal of this project is to empower a subscription-based or retail business to gain deeper insights into its customer base by effectively segmenting customers. This segmentation is based on critical factors such as income, spending habits, and churn risk. By leveraging these insights, the business can implement more targeted marketing strategies, enhance customer retention, and ultimately reduce churn through an interactive, automated Excel dashboard.

---

## **Data Sources & Assumptions** 📊

### **Data Sources**:
- **Sales Data**: This dataset includes customer transactions, capturing essential details like Customer ID, monthly spend, annual income, and contract type. This data is fundamental for understanding financial interactions.
- **Customer Data**: This includes demographic information such as age, city of residence, income bracket, and loyalty score. Understanding these demographics helps tailor marketing efforts.
- **Churn Data**: This dataset identifies whether a customer has churned or is at risk of doing so, categorized by risk levels. This is crucial for proactive retention strategies.

### **Key Data Columns**:
- **Customer_ID**: A unique identifier for each customer, essential for data integrity and lookups.
- **Customer_Name**: The name of the customer, utilized for validation and enhancing user experience in data lookups.
- **Annual_Income**: The total income of the customer for the year, important for income-based segmentation.
- **Monthly_Spend**: The average monthly expenditure of the customer, which informs spend-related analyses.
- **Churn Risk**: An indicator reflecting the likelihood of customer churn, derived from various metrics.
- **Loyalty Scores**: A proprietary metric indicating the level of customer loyalty based on engagement and tenure.
- **Contract Type**: Describes the nature of the customer’s subscription or service agreement, influencing retention strategies.
- **Customer_Tenure**: The length of time the customer has been associated with the business, crucial for understanding customer loyalty and engagement.
- **Service_Usage**: Measures the extent to which the customer utilizes the business’s services, helping identify potential churn risks.
- **Age Group**: Classifies customers into demographic brackets (e.g., Young Adult, Mature Adult), which aids in targeted marketing.
- **City**: The geographical location of the customer, allowing for localized marketing efforts.

---

### **Assumptions**:
1. **Churn Risk Calculation**: It is assumed that churn risk is determined by a combination of service usage and customer tenure, which are both critical indicators.
2. **Loyalty Scores**: Loyalty is calculated using a proprietary model that factors in tenure, spending patterns, and customer engagement levels.
3. **Income Segmentation**: Customers are classified into income brackets (e.g., Low, Middle, High Income) based on their annual income for targeted marketing.
4. **Consistent Data Updates**: The sales table is linked using `XLOOKUP`, ensuring real-time updates whenever new sales data is added, facilitating timely decision-making.
5. **Churn Probability Accuracy**: It is assumed that churn risk scores provided are accurate and based on historical data analyses.
6. **Data Completeness**: The dataset is assumed to contain all necessary fields without significant missing values, ensuring robust analysis.

---

## **Techniques and Excel Formulas Used** 💻

### **1. Data Cleaning and Transformation** 🧹
- **Duplicate Management**: Employed Excel’s `Remove Duplicates` function to ensure that only unique customer entries are retained, thus preventing data inconsistencies.
- **Formatting Consistency**: Applied consistent formatting for numbers and dates using the `TEXT` function and custom formats to maintain uniformity throughout the dataset.
    - Example: `=TEXT(A2, "dd-mmm-yyyy")` ensures all dates follow the same format.
- **Text Functions**: Utilized `PROPER`, `TRIM`, and `SUBSTITUTE` to standardize text entries, particularly for customer names, ensuring clarity and accuracy.
    - Example: `=PROPER(TRIM(SUBSTITUTE(A2," ","")))` cleans names by removing extra spaces and correcting capitalization.

### **2. Lookup and Reference Automation** 🔗
- **XLOOKUP**: Leveraged for dynamically retrieving related data based on Customer ID, enhancing the dashboard’s interactivity.
    - Example: `=XLOOKUP(Customer_ID, DataTable[Customer_ID], DataTable[Annual_Income])` pulls annual income based on Customer ID.
- **INDEX MATCH**: Implemented for more complex data retrieval scenarios where XLOOKUP is not applicable, allowing for enhanced flexibility in data analysis.
    - Example: `=INDEX(Table2[Income], MATCH(Customer_ID, Table1[Customer_ID], 0))` facilitates cross-referencing data across different tables.

### **3. Data Enrichment with Power Query** ⚙️
- **Data Cleaning**: Used Power Query to remove null values, rectify inconsistencies, and split full names into first and last names, streamlining the dataset for analysis.
- **Custom Columns**: Added custom columns to derive additional metrics, such as income brackets and loyalty categories, which support segmentation efforts.

### **4. Pivot Tables & Descriptive Analysis** 📊
- **Pivot Tables**: Created to summarize and analyze customer segmentation by demographics such as city, income, and tenure, facilitating deeper insights.
- **Descriptive Statistics**: Utilized Excel’s Data Analysis Toolpak to calculate key statistics (e.g., averages, counts, standard deviations) for various customer groups, enhancing the analytical framework.

### **5. Dynamic Charts and Visualizations** 📈
- **Quadrant Chart for Customer Segmentation**: Developed a scatter plot to visualize income against spending, categorizing customers into four quadrants (e.g., High Income/High Spend).
    - This visualization helps identify customer groups for targeted marketing strategies.
- **Bubble Chart for Loyalty vs. Churn Risk**: Created to illustrate the relationship between loyalty scores and churn risk, with bubble sizes representing monthly spend.
    - This chart highlights high-risk segments that require attention.
- **Churn Probability Heatmap**: Visualized churn risk across demographic attributes using conditional formatting and heatmap color scales, allowing for quick assessments of high-risk groups.
- **Retention by Contract Type (Stacked Column Chart)**: Summarized retention rates by contract type, facilitating insights into which contracts yield better customer loyalty.

### **6. Filtering & Data Validation** 🔧
- **Dynamic Dropdown Filters**: Implemented data validation to create dropdowns for filtering by attributes such as city, income bracket, and age group, enhancing user interactivity.
    - Example: 
      ```excel
      =FILTER(Customer_Data[City], Customer_Data[Income_Bracket] = Selected_Bracket)
      ```
- **Interactive Slicers**: Added slicers to enable users to dynamically filter data by various demographic groups, promoting a user-friendly interface for exploration.

---

## **Findings & Insights** 🔍

### **1. High-Value Customers**:
- **Insight**: Customers in the high-income, high-spend quadrant demonstrate significantly lower churn risk. Targeted marketing efforts can focus on retaining these valuable segments through personalized outreach and loyalty programs.

### **2. Churn Risk**:
- **Insight**: Customers exhibiting lower loyalty scores coupled with medium spending are identified as being at a higher risk of churn. Implementing targeted retention strategies, such as personalized loyalty rewards, may mitigate this risk.

### **3. Contract Type and Retention**:
- **Insight**: Data indicates that customers with long-term contracts (e.g., annual subscriptions) exhibit higher retention rates. Providing incentives for transitioning customers to longer-term agreements can enhance overall retention.

### **4. Customer Spending & Tenure**:
- **Insight**: Analysis reveals that while monthly spending typically increases during the initial years of a customer’s tenure, it plateaus after three years. This suggests that businesses should focus on engaging customers in the early stages to maximize lifetime value.

---

## **Implementation Steps** 🔄

### **1. Data Cleaning & Setup**:
- Import raw customer data into Excel and utilize Power Query for initial transformations.
- Clean the dataset by removing duplicates, standardizing formats, and categorizing customers into segments.

### **2. Formula Setup**:
- Establish all necessary lookup formulas (e.g., `XLOOKUP`, `INDEX MATCH`) to ensure dynamic data retrieval for each customer entry.
- Create calculated fields for key metrics such as loyalty scores, income brackets, and churn risk.

### **3. Pivot Tables & Charts**:
- Develop pivot tables for each analytical segment (e.g., churn analysis, retention by contract type).
- Create dynamic visualizations using charts (scatter, bubble, heatmap) that link to pivot tables and respond to dropdown filters.

### **4. Automation & Integration**:
- Enable Power Query automation so that the dashboard updates automatically with new data upon refresh.
- Ensure seamless connections between data tables and visual elements to facilitate user interactions.

---

## **Conclusion** ✅

This project successfully delivered a robust, automated Excel dashboard that significantly improves the client's ability to segment customers, predict churn, and enhance retention strategies. By employing advanced Excel techniques such as Power Query, dynamic charts, and data validation, the dashboard provides a real-time, scalable solution for data-driven decision-making based on customer behavior.

**Key Outcomes**:
- Enhanced customer retention through targeted strategies for high-risk segments.
- Deeper insights into customer behavior across varying income and spending categories.
- Automated reporting processes that minimize manual efforts and facilitate seamless data integration.

---

## **Future Enhancements** 📈
- Incorporate advanced predictive analytics models (e.g., logistic regression) for more precise churn predictions.
- Integrate the dashboard with Power BI for more interactive, cloud-based reporting options.
- Expand segmentation capabilities to include detailed insights based on customer service usage patterns and behaviors.

---

