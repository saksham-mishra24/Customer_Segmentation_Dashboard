# 🌟 Customer Segmentation & Targeting Dashboard 🌟

**🔍 Industry**: Retail  
**📊 Domain**: Customer Segmentation & Targeting  
**🛠️ Tools Used**: Microsoft Excel, Power Query  
**🔧 Techniques Applied**: Data Cleaning, Descriptive Statistics, XLOOKUP, INDEX MATCH, Pivot Tables, Dynamic Charts, Power Query 🔍

---

## **Project Overview** 🚀
Welcome to the **Customer Segmentation & Targeting Dashboard**! This project focuses on using data to help retail businesses better understand their customers. The goal is to transform raw customer data into clear insights that guide marketing strategies and improve customer relationships. By creating a dynamic, user-friendly dashboard, we enable the client to analyze customer behavior through segmentation based on key attributes such as age, city, income, and spending patterns.


---

## **Client's Challenge** 💼
The client wanted to improve their marketing efforts but struggled to understand customer demographics and behaviors. They needed a tool that could visualize customer segments easily and update automatically as new data came in. The main objectives were:

- **Automating** data processing
- **Organizing** customer data
- **Creating** an interactive dashboard for better marketing insights

---

## **Project Implementation** 🔄


### **Situation**
The initial dataset provided by the client was unstructured, containing inconsistent formats, null values, and duplicate records. The need arose to clean, categorize, and link this data so that visuals would update automatically as new data was integrated.


### **Task**
I was responsible for transforming the raw customer data into a structured format, automating key calculations, and designing interactive visuals (including pie charts and pivot tables) to showcase customer segments dynamically.



### **Actions Taken** 🎯

1. **Data Cleaning and Transformation** 🧹:
   - **Duplicate Management**: Utilized Excel shortcuts (`Alt + A + E`) to identify and remove duplicates, ensuring data integrity.
   - **Date and Number Formatting**: Standardized date formats (`dd-mmm-yyyy`) and applied number formatting to maintain consistency.
   - **Customer Categorization**: Employed multiple `IF` functions to classify customers into specific **age groups**, **loyalty categories**, and **spending brackets**.
   - **Text Functions**: Leveraged functions like `CONCAT`, `SUBSTITUTE`, and `PROPER` to standardize inconsistent text entries.
   - **Data Organization**: Converted ranges into tables to facilitate effective data management and analysis.

2. **Lookup Automation** 🔗:
   - Implemented **XLOOKUP** and **INDEX MATCH** functions to automate data retrieval across linked tables, ensuring that the dashboard remained dynamic with new entries.

3. **Data Enrichment via Power Query** ⚙️:
   - Cleansed the dataset by removing null values, trimming excess spaces, and splitting names into **first** and **last names**. Custom columns for **salary brackets** and **loyalty categories** were added using **Power Query**.

4. **Descriptive Analysis and Pivot Tables** 📈:
   - Employed Excel’s **Data Analysis Toolpak** to generate comprehensive descriptive statistics for customer demographics and spending behaviors.
   - Created a series of **pivot tables** and **pivot charts** to summarize data effectively and facilitate quick insights. 
   - Integrated **timelines** for trend visualization and added **dynamic slicers** to enhance interactivity.

5. **Dynamic Visualization** 📊:
   - Developed a **dynamic pie chart** to visualize customer segmentation by age group, adjustable based on selected cities.
   - Incorporated **Data Validation** to create multiple dropdown filters that automatically updates the corresponding visuals using `COUNTIFS` and `FILTER()` functions.
   - **Data Validation Filtering**: Implemented data validation for filtering attributes so that when any attribute is selected, the dashboard dynamically filters accordingly without using slicers. For instance, formulas such as:  
   - Connected **tables** to ensure that updates to sales data automatically reflected in the customer segmentation chart, employing multiplication formulas for sales calculations.

6. **Automation and Integration** 🔄:
   - Designed the workflow to allow for seamless integration of new datasets. The dashboard updates automatically with a simple refresh action, thanks to the efficient linking of datasets and table conversions.

### Results 🎉
- **Enhanced Data Quality**: All customer records were meticulously cleaned, organized, and categorized, resulting in a more accurate analysis.
- **Automated Dashboard**: The client now benefits from a real-time updating dashboard that requires no manual intervention for new data entries.
- **Actionable Insights**: Dynamic visuals, including **pie charts**, **pivot tables**, and comprehensive summaries, empower the client to identify and effectively target specific customer segments for marketing campaigns.
- **Efficiency Gains**: Automation reduced the need for manual recalculations, significantly saving time on regular reporting tasks.

---


## **Conclusion** ✅
This Excel dashboard provided the client with a powerful tool for customer segmentation and better decision-making. By using Excel's advanced features, along with dynamic visuals and Power Query, I successfully met the client’s need for real-time insights into customer behavior. This project highlights how Excel can create flexible and automated solutions for analyzing large-scale retail data.


---


## **Final Thoughts** 💡
Thank you for checking out this project! I hope it inspires you to explore data analysis in your work. If you have any questions or ideas for collaboration, please feel free to reach out. Happy analyzing! 😊🌟
