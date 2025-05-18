# UK Bank Customers Dashboard Analysis
This repositrory contains my Power BI dashboard project focused on segmenting UK bank customers based on various demografic and financial attributes. The dashoboard allows for interactive exploration of customer data accross diffrenet regions of the UK.



## Visualizations

* **Map:** Showing data broken down by region (England , Northern Ireland, Scotland, Wales).

* **Distribution by Age:** A histogram showing the percentage of customers within different age bins.
```dax
 Percentage of Customers by Age = 
DIVIDE(
    COUNT('UK-Bank-Customers'[Customer ID]),
    CALCULATE(COUNT('UK-Bank-Customers'[Customer ID]),
ALL('UK-Bank-Customers'[Age (bins)]))
)
```
Formated to see as percentage with 0 decimal places

* **Gender:** A pie chart illustrating the distribution of customers by gender.

* **Distribution by Balance:** Another histogram showing the percentage of customers within different balance bins.
```dax
Percentage of Customers by Balance = 
DIVIDE(
    COUNT('UK-Bank-Customers'[Customer ID]), 
    CALCULATE(COUNT('UK-Bank-Customers'[Customer ID]), ALL('UK-Bank-Customers'[Balance (bins)])) 
)
```

* **Job Classification:** A treemap displaying the proportion of customers in differenet job classifications (White Collar, Blue Collar, Other).
```dax
Total Customers by job classification =
CALCULATE(COUNTROWS('UK-Bank-Customers'),
ALL('UK-Bank-Customers'[Job Classification])
)
```



## Further Analysis

The dashboard can be used for further analysis, such as:

* Identifying target customer segments for specific products or services in different regions.
* Understanding the demographic and fianncial profiles of customers in various parts of UK.
* Comparing customer characteristics across different job classifications



## To Use This Respiratory

1. *(If applicable) Download the Power BI .pbix file.*
2. *(If appliacable) Open the  .pbix file in Microsoft Power BI Desktop.*
3. Interact with the filters and visualizations to explore the data.




## Example of Insights from UK Bank Customer Segmentation Dashboard

* **Diferent Customer Density:** The total customer count is displayed at the top of the dashboard and changes significantly with each region selected on themap. This highlights differences in customer concentration across the UK. For instance, when **England** is selected, the customer volume is much higher compared to when smaller region like **WALES** is selected. This suggets much larger population density of bank customers in England compared to Wales. 
  

*  **Regional Age Profile Changes:** The "Distribution by Age" chart demonstrates that the dominant age groups and the overall age distribution of customers are not uniform across all regions. Diffrent areas have different age peak ranges. For example, the age distribution in ** Scotland** is showing higher percentage in the ** 40-50 age group** compared to **England**, where the peak is in the **30-40 agegroup**. This could indicate different demographic trends and bank could start focusing on  offering more packages for specific age groups in different region. 

*  **Gender Imbalance Across Regions:** The "Gender" pie charts shows that the proportion of male and female customers is different in each area and is not consistend throught the UK. For example, **Norhern Ireland** might show a slightly higher proportion of **male customers** compared to **England**, where the balance is closer to even. Or **Wales**, where is higher proportion of **woman customers**. Different could be linked to regional emplyment or social factors. 

*  **Geographical Balance Distribution:** The "Distribution by Balance" show that the financial profiles, indicated by account balances, differ across regions. Some areas have a higher concentration of higher or lower balance holders. For instance, **Wales** balance distribution is concentradet in the mid-range , whre, for example, in **Scotland** is balance distribution more towards lower ranges, showing a different economical profile.

*  **Job sector Concentration:**  It reveals that the representation of different job sectrors among bank customers is not evenly distributed across UK. For example, **Scotland** has a larger "Blue Collar" segment compared to **England**, that has  larger "White Collar" segment. **Northern Ireland** shows a different distribution in the "Other" category, reflecting a unique landscape in that region. 



 ## Conclusion & Strategic Implications

Regional analysis reveals significant customer differences across the UK. The bank should adopt tailored strategies for product offerings, marketing, branch services and risk management in England, Scotland, Wales and Northern Ireland to optimize profitability in each each market. 
Understanding regional variations in customer profiles is very important. Implementing localized strategies wil allow bank to better serve diverse needs and enhance its competitiveness across the UK. 







