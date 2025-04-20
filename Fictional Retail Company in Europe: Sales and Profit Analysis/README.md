# Sales and Profit Dashboard - Project Steps

1.	**Uploaded Data** - Imported a Microsoft Excel workbook into Power BI. Ny data were already clean and reliable, so it wasn't necessary to use Power Query. If needed I can make some transformation later. Modelling was automatically generated with Power BI. The key relationship was established on Order ID column. 
2.	**Created Hierarchy** (called Geography in ListOfOrders table) - Organized data into hierarchical structure for better analysis and visualization. Geography = Country » State » City 
Important: If error message: File->Options and Settings -> Options -> Security -> Map and Filled Maps Visuals -> ENABLE
3.	**Created Map**- using Geography in Location Field and to reinforced it with Latitude and Longitude fields.  Initially Latitude and Longitude were aggregated as an average but I change it to the Median. Since the latitude and longitude values represent cities in the dataset, using the Median provides a more accurate alignment when drilling up to state level in hierarchy
Bubble size-> Sum of Sales
Calculated Measure: Profit Margin - Sum of Profit/Sum of Sales *100 (%)
 
Profit Margin = SUM(OrderBreakdown[Profit])/ SUM(OrderBreakdown[Sales])
 
Formatted Bubbles-> Colors-> Conditional Formatting -> Gradient style based on Profit Margin filed
 
Size of the Bubble:  tells me size of the sales
Color of the Bubble: tells me how large or low is a Profit Margin for each of this Countries, States, Cities 
 
Example Analyzing:
Netherlands - low Profit Margin as well low Sales 
Ireland - low number of Sales and low Profit Margin
Uk - large number of Sales and large Profit Margin
Germany - darker than UK, is very good in both, Sales and Profits…
 
 
 
4.	**Created Scatter Chart** - X-axis Sum of Sales, Y-axis Sum of Profit from OrderBreakdown Table, for our level of Granularity I placed in Values field Customer Name 
 
Formatted Markers -> Colors -> Conditional Formatting ->Gradient
 
I applied Filter on All Pages - Order Date 
Advanced Setting -> On or After 1/1/2011 AND Before 12/31/2013 (2 years period) -> Apply Filter -> FILTER REMOVED FOR NOW 
 
5.	**Created new Page  DASHBOARD ** Copy_Paste Page 1 and Page 2
Scatter Chart -> Filter -> Legend -> Off
Add Slicer -> Order Date
Add Slicer -> Country - I will do a Bookmarks later change slicer to Segment
In Segment -> Format -> Slizer Settings -> Tile
 
Scatter Chart Adjust Range
y-Axis Min: Auto -> -4000, Max: Auto ->6000
x-Axis Min: Auto ->0, Max: Auto -> 17000
 
6.	**Added Donut Chart** - we need one numerical variable and one categorical variable.
Values -> Sum of Profit
Legend -> Category
 
7.	**I created page to show the countries with best and worst performance based on Total Profit, can filtered by categories.**
By choosing for y-axis Profit Margin, I would point out countries most efficient at generating profit. My intention was to show countries that brought in the most profit, that why  I used Total Profit Summary. 
 
8.	**Added Bookmarks**
View - Bookmarks -> Add - Most profitable country based on total summary of profit
View -> Bookmarks -> Add - Least profitable country based on total summary of profit
 
Insert Blank Button -> Action -> Bookmark-> choose Bookmark and filtering (text, color, tooltip) 
 
9.	**Organize my Dashboard**
Visual -> Shadow ->On 
 
Add card -> with value Sum of Profit, 
Formatting card
Callout value ->Font 15 
Category Label -> remove 
 
Formatting Donut chart:
Lebel Contents - > Percent of Total
Percentage decimal places -> 0
 
Format-> Edit interaction -> select filter on Donut chart, not to see history when selecting Country, State, City
