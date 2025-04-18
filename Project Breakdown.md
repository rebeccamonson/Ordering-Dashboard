## Ordering Data Dashboard Creation

<p align="center">
  <img src="Images/box.png" alt="boxes" width="400"/>
</p>

The hospital provided one large excel file with several worksheets in it related to supplier data. This data was uploaded into Power BI for the majority of the data cleaning and exploration 
process. Overall, the data was very clean and required little editing. To create the desired visuals in PowerBI, several new variables were created. 

## Variable Creation and Management 🌸

Below is a table of the newly created variables in PowerBI along with the DAX code used to create them. 

<p align="center">
  <img src="Images/datadict1.png" alt="datadict" width="400"/>
</p>

<p align="center">
  <img src="Images/datadict2.png" alt="datadict" width="400"/>
</p>

## Order Date Page 📆
---
This page contains visuals for number of orders over time, total spent per order over time, average order size by month, and count of orders per day of week. It has a slicer option to filter 
the visual by month or year. 

<p align="center">
  <img src="Images/order-date-full.png" alt="Order Date Page w/o Filter" width="600"/>
</p>
<p align="center">The Order Date page without filters </p>

<p align="center">
  <img src="Images/order-date-date.png" alt="Order Date Page w Filter" width="600"/>
</p>
<p align="center">The Order Date page with a filter for Feb </p>


**Significance Testing 🏁**

Because the hospital was curious about if there were any trends in the ordering where there were days with a significant amount of spending or a significant amount of orders being placed. 
If the tool flagged a day as beign significant, the hospital could go back and investigate what took place that would cause a signifcant uptick in spending or ordering. Testing was done 
using two different methods: 

* **Z Scores**: the Z Score method was used to determine if there were any days that had a s significant number of orders compared to the average. The average and standard deviation were
  calculated to accomplish this. After Z scores were calculated using the DAX code to create the Z Score formula, the threshold of 2 was set and the signifance was applied to a tool tip
  feature that will display is the significance level was normal or not.

* **IQR Method**: the IQR method was used to test for outlier days with significant spending. The Q1 and Q3 were both calculated, and then used to calculate the interquartile range. Days
  outside of this range were flagged as outliers by a measure created in DAX code. This feature was also applied to a tool tip that would display if it was significant or not.

<p align="center">
  <img src="Images/order-count-filter.png" alt="Order Date Page w/o Filter" width="600"/>
</p>
<p align="center">Order Count Visual with tooltip </p>


<p align="center">
  <img src="Images/total-spent-fitler.png" alt="Order Date Page w/o Filter" width="600"/>
</p>
<p align="center">Total Spent Visual with tooltip </p>

## Supplier Page 🗂️
---
This page contains a breakdown of the data related to the three suppleirs utilized by the hospital. The hospital was espeically interested in comparing the prices of items from multiple 
suppliers. While it might sometimes be necessary due to order an item from a suppleir regardless of price due to availabiltiy, the hsopital would like to try and always purchase items 
from the supplier with the lowest price. They were also interested in seeing what category of items are ordered from which suppliers and total spent over time. 


<p align="center">
  <img src="Images/order-date.png" alt="Order Supplier Page" width="600"/>
</p>
<p align="center">Unfiltered Supplier Page </p>

This supplier page can also be filtered down by supplier. 

<p align="center">
  <img src="Images/bysupplier.png" alt="Order Supplier Page filtered" width="600"/>
</p>
<p align="center">Filtered Supplier Page </p>

## Procedure Estimation Page 💵
---
A large portion of this project was focused on estimating the item and numbers of items needed for a given surgery for a specific surgeon. This was the main goal to assist in inventory
management for the hopsital staff and this page can display the needed supplies and their quantity for weekly ordering. The page is capable of being filtered by surgeon and procedure,
as several of the surgeons perform more than type of procedure. Addtionally, this page can display the estimated supply cost for the hospital. This page also displays the top five most 
expensive items ordered for each surgeon. 


<p align="center">
  <img src="Images/shoulder-filter.png" alt="Order Supplier Page filtered" width="600"/>
</p>
<p align="center"> Surgeon page filter by surgeon 4 and shoulder </p>

This page has been formatted to display a table that shows the needed items, their quantity, their category, their price, and the last order date for the item. Conditional formatting 
was applied to the order date column so that items ordered within the last 30 days would green, the last 60 would be yellow, and anything beyond 60 would be red. This is just to 
highlight any potential items that may need to be followed up on to ensure adequate inventory levels. 

<p align="center">
  <img src="Images/spine-filter.png" alt="Order Supplier Page filtered" width="600"/>
</p>
<p align="center"> Surgeon page filter by surgeon 4 and spine </p>

## Start Page 🏁

The first page of the dashboard tool is designed to be a general summary page of the most recent ordering data. From this page you can drill through to the more detailed pages that 
give a more focused look into order date, suppliers, and supply estimation. The start page features summary information such as: 

* date of last order placed
* total orders placed this month
* total spent this month
* links to supplier ordering login pages
* bar chart comparing monthly spend from this year to last year

✨ This page is currrently still under construction, check back later for updates! ✨



