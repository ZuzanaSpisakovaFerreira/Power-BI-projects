# Bank Customers Dashboard - Project steps

**1. MAP** 
Field Map -> Region  to Legend and Location
Filters Auto Zoom -> Off
Inserted card -> with Customer ID and filtered
 
**2.	Created Pie Chart for Genders**
Legend - Gender
Values - Count of Customer ID
Filtered (Lebels, colours etc)
 
**3.	I created Bins and Distributions for Age**
Created Age Bins 
Right click --> Group -- I `ve chosen bin size 5 
Created Chart- -> Distributions for Balance 
X - Axis - Age Bins
Y- Axis -Count  Customers ID - -> I changed for Customer ID Percentage by Age bins: 
I created a new  measure Percentage of Customer ID for Age Bins specifically,
 
DAX Formula: 
 
Percentage of Customers by Age = 
DIVIDE(
    COUNT('UK-Bank-Customers'[Customer ID]),  // Replace 'UK-Bank-Customers' and 'CustomerID'
    CALCULATE(COUNT('UK-Bank-Customers'[Customer ID]), ALL('UK-Bank-Customers'[Age (bins)])) // Replace 'UK-Bank-Customers' and 'AgeBin'
 
 
Formatted it to see as  percentage  with 0 decimal places 
 
 
 
**4.	I created Bins and Distributions for Balance **
I created Bins  every 10 000 (pounds) --> Right clicked --> Create Groups --> Balance Bins 
X-  Axis - Balance Bins
Y - Axis - Count of Customer ID --> again I calculated a new measure Percentage of Customers by Balance  based on Balance Bins.
 
Formula :
 
Percentage of Customers by Balance = 
DIVIDE(
    COUNT('UK-Bank-Customers'[Customer ID]),  // Replace 'UK-Bank-Customers' and 'CustomerID'
    CALCULATE(COUNT('UK-Bank-Customers'[Customer ID]), ALL('UK-Bank-Customers'[Balance (bins)])) // Replace 'UK-Bank-Customers' and 'Balance (bins)'
)
 
  
 
 
**5.	Job classification Treemap chart**
Tree map:
Category-->Job classification
Values --> I calculated Percentage of customers by  Job classification 
 
a.	I created a new measure and calculated Total customers count across categories filtered by job classification
 
Formula:
 
Total Customers by job classification = CALCULATE(COUNTROWS('UK-Bank-Customers'), ALL('UK-Bank-Customers'[Job Classification]))
 
b.	I calculated the Percentage of each category
 
Formula: 
 
Percentage of Customers by job classification = 
DIVIDE(
    COUNTROWS('UK-Bank-Customers'),
    [Total Customers by job classification])
 
c.	I formatted to format Percentage with 0 decimal places
