# Indian Agriculture Analysis 

# Dashboard Link : https://app.powerbi.com/groups/me/dashboards/bee98ffc-53a5-40d5-8626-42a87484ee3c?ctid=9eaedd8f-a5a0-4133-94f2-85f78b91d510&pbi_source=linkShare

# Problem Statement

This dashboard provides an in-depth analysis of Indian agriculture. It helps stakeholders understand trends in crop production, seasonal variations, and state-wise agricultural output. The dashboard enables policymakers, farmers, and analysts to make informed decisions based on data-driven insights.

### Steps Followed

# Step 1: Data Preparation

Loaded the dataset into Power BI Desktop. The dataset was in CSV format.

Opened the Power Query Editor to inspect data quality.

Checked for missing values and errors using "Column Distribution," "Column Quality," and "Column Profile."

Observed that all columns had valid data with no missing values.

# Step 2: Data Cleaning and Transformation

Ensured all numerical columns were in the correct format.

Verified that "Area" and "Production" had no extreme outliers affecting analysis.

Created calculated columns and measures using DAX for further analysis.

# Step 3: Visualizations and Insights

State-Wise Crop Production: Used a filled map to represent the total production per state.

Top Crops by Production: Created a bar chart ranking the highest-producing crops.

Seasonal Production Trends: Used a line chart to compare production trends across different seasons.

Yearly Production Analysis: Analyzed trends in agricultural production over different years using a line graph.

Crop Distribution by Area: Created a tree map to visualize how different crops are distributed in terms of cultivated area.

District-Level Analysis: Provided a detailed view of agricultural output at the district level using a table visual.

# Step 4: Key Measures in Power BI (DAX Expressions Used)

# Total Production:

Total Production = SUM(Indian_Agriculture[Production])

# Total Area Cultivated:

Total Area = SUM(Indian_Agriculture[Area])

# Average Yield (Production per Hectare):

Avg Yield = DIVIDE(SUM(Indian_Agriculture[Production]), SUM(Indian_Agriculture[Area]))

# Top Crop by State:

Top Crop = TOPN(1, SUMMARIZE(Indian_Agriculture, Indian_Agriculture[State_Name], Indian_Agriculture[Crop], "Total Production", SUM(Indian_Agriculture[Production])), [Total Production], DESC)

# Step 5: Report Design

Added slicers to filter data by State, District, Year, Season, and Crop.

Applied a consistent theme to maintain visual clarity.

Used tooltips to provide additional insights when hovering over charts.

Added text boxes to highlight key insights and recommendations.

# Insights from the Dashboard

# 1. State-Wise Analysis

The top states with the highest agricultural production include Uttar Pradesh, Punjab, and Maharashtra.

Some states specialize in specific crops, e.g., Punjab leads in wheat production, while Maharashtra excels in sugarcane production.

# 2. Seasonal Trends

Kharif season shows the highest production levels due to monsoon-dependent crops like rice and maize.

Rabi crops like wheat and barley perform well in the northern states.

# 3. Crop-Wise Production

Rice and wheat dominate Indian agriculture in terms of production volume.

Commercial crops like sugarcane and cotton contribute significantly to the economy.

# 4. District-Level Insights

Some districts within states produce disproportionately high quantities of certain crops.

Punjab’s Ludhiana and Amritsar contribute heavily to wheat production.

# 5. Area vs. Yield Efficiency

Some states have large cultivated areas but low yields due to poor irrigation and soil conditions.

Tamil Nadu and Andhra Pradesh show high yield efficiency despite smaller cultivation areas.

# Report Snapshot (Power BI DESKTOP)

 
![Image](https://github.com/user-attachments/assets/984dab23-fb13-431a-acc2-a7a9b92de16c)

![Image](https://github.com/user-attachments/assets/4d16724c-4d87-4e01-833e-c07287b040cc)
# Conclusion

The Power BI dashboard offers a comprehensive view of Indian agriculture, highlighting trends, key contributors, and areas for improvement. These insights can help improve agricultural planning, policy formulation, and investment decisions in the sector.

