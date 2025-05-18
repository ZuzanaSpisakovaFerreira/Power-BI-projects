# Sales and Profit Dashboard

This Power BI dashboard provides an interactive analysis of sales and profitability data. It offer clear visualizations and insights into key performance indicators such as geographical sales distribution, profitability acoss customer segments and performance by product categories over a specific period (2011-2014).

## Visualizations

* **Geographic Map:** Displays sales and profit margin across diferent countries in Europ, with bubble size indicating sales volume and colour representing profitability. **The profit margin is calculated using the following DAX formula:**
  ```dax
  Profit Margin =
  SUM(OrderBreakdown[Profit])/ SUM(OrderBreakdown[Sales])

*  **Scatter Chart:** Ilustrates the relationship between the sum of sales (X-axis) and the sum of profit (Y-axis) for individual customers. The colour of the bubbles represents gradient based on profitability.


*  **Donut Chart:**  Shows the **Sum of Profit by Category**. Each segment represents a different product category (Office Supplies, Technology, Furniture) and the size of the segments show the proportion of the total profit contributed by that category. The values and percentages of each category are also displayed

*  **Slicer - Order Date:** Allows users to interactively filter the data by selecting a specific date range using a slider. The range shown is from 1. January 2011 to 31. December 2014.

*  **Slicer - Segment:** Enables to filter the data based on customer segments: Consumer, Corporate and Home Office. Users can select one or multiple segments to focus their analysis.

*  **Underperformance Button:** When clicked, this button filters the dashboard to display **three countries with the lowest profit margin**. This allows users to quickly identify the regions where profibility is weakest.

*  **Top performers Button:**  Clicking this button filters the dashboard to show **three countries with the highest profit margin**. This enables users to focus on most profitable regions and understand the factors contribuiting to their sucess.


  ## Example Insights and Key Findings from the Dahboard

* **Top Performing Countries (Profit Margin Leaders):** Three countries withthe highest profit margins are the **UK**, **Germany** and **France**. These markets are our **most profitable** in terms of the percentage of revenue we keep as profit. Company should closely examine the factors contributing to their sucess. 

 *  **Areas for Improvement (Lower Profit Margin):** The countries with the lowest profit margins are **Portugal**, **Sweden** and **Netherland**. Here we need to  investigate the reason behind lower profitability and explore pottential startegies for improvement. While the **Netherlands** have a decent sales volume, the profit generated from this sales is low.

 *  **Geographic Picture:** The map provides a quick visual overview of sales volume. You can drill down to city level and this allows you quickly identify high-performing and low-performing regions, cities and even specific customers. For example map shows that UK and Germany have largest sale sbubbles , indicating high sales volume. The colour of the bubbles reveals profit margin. The netherlands, for example has a low profit margin. Ireland, opposite, has a low number of sales but high- profit margin. Is good to invetsigate the reason behind this.

 *  **Key Customers:**  The scatter chart help us identify our most valuable customers, enabling us focus on strengthening those relationships. Customers in the upper right quadrant are high sales, high profit, while those in lowe left are low sales, low profit. 

 *  **Top Product Categories (Profit Drivers):** The donut chart clearly indicates which product categories contribute the most to overall profit. We can examine for each country, city  which product is the biggest drivers to our earnings.

 *  **Order Date and Segment:** They allow us to analyze trends over time  and compare the performance of different customer types.



## Conclusions 

This Sales and Profit dashboard is offering powerful and interactive tool for analyzing key aspects of  retail performance for our fictional company. Thanks to this dashboard , the company can analyze its strenght and weaknesses across different markets, customer segments and product lines. It help us to make a strategic desicions:

* Focusing investments in the most profitable areas
* Developing strategies to improve profitability in less sucessful regions and product lines
* Understanding and taking care of our most valuable customers.

Ultimately, this dashboard enables company to drive sustainable growth and overall profitability. 
