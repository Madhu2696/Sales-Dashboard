# Task-1-PBI


#### SALES DASHBOARD ####

Power BI dashboard showing sales trends, top products, and regional performance using sample data

Step 1: Collect Sample Data
Can create a simple Excel dataset or use an existing dataset that contains:
Sales data (e.g., Date, Product, Region, Sales Amount, Quantity)
Product data (e.g., Product Name, Category, Price)
Region data (e.g., Region Name, Region Sales Target, etc.)

Step 2: Load Data into Power BI
Open Power BI Desktop.
Go to the Home tab, then select Get Data.
Choose the Excel option (or any other data source you're using), and select the file containing your sales, product, and region data.
Load all tables into Power BI.

Step 3: Create Relationships
Go to the Model view 
Create relationships between tables:
Sales Data → Product Data: Connect Product to Product Name.
Sales Data → Region Data: Connect Region to Region Name.

Step 4: Create Measures (DAX formulas)
In Power BI, you’ll need to create some DAX measures to aggregate your data:
1.Total Sales:Total Sales = SUM('Sales Data'[Sales Amount])
2.Total Quantity:Total Quantity = SUM('Sales Data'[Quantity])
3.Average Sales per Day:Avg Sales per Day = AVERAGE('Sales Data'  [Sales Amount])
4.Sales vs Target:
Sales vs Target = 
VAR Total_Sales = [Total Sales]
VAR Target = SUM('Region Data'[Sales Target])
RETURN Total_Sales / Target

Step 5: Build the Dashboard Visuals
1. Sales Trends 
X-Axis: Date
Y-Axis: Total Sales
Legend: Region or Product (to compare by region or product)
This line chart will show the trend of sales over time.

2. Top Products 
X-Axis: Total Sales
Y-Axis: Product

3. Regional Performance 
X-Axis: Region
Y-Axis: Total Sales
Tooltip: Sales vs Target measure
This clustered column chart compares the total sales by region 

4. Sales vs Target 
Measure: Sales vs Target
This gauge or KPI visual will display how sales are tracking against the regional sales targets.

5. Sales by Product Category 
Legend: Category (from the Product Data)
Values: Total Sales
This pie chart will break down total sales by product category (e.g., Electronics, Furniture).

Step 6: Design and Format the Dashboard
Use consistent colors for regions or products for better clarity.
Add slicers to filter by Date, Region, and Product.
Organize the visuals on the dashboard for easy navigation.
Format titles, axis labels, and data labels for better readability.

Step 7: Publish and Share the Dashboard

Publish it to the Power BI Service by clicking Publish in Power BI Desktop.
This setup will give a comprehensive view of the sales data and allow to analyze trends, product performance, and region data success in one dashboard.


Sales Dashboard Output

![Image](https://github.com/user-attachments/assets/66592708-37f3-491e-b600-853d4991a495)





