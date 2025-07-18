# Kultra Mega Stores Inventory
#### Kultra Mega Stores (KMS), headquartered in Lagos, specialises in office supplies and furniture. Its customer base includes individual consumers, small businesses (retail), and large corporate clients (wholesale) across Lagos, Nigeria.
#### I have been engaged as a Business Intelligence Analyst to support the Abuja division ofKMS. The Business Manager has shared an Excel file containing order data from 2009 to 2012 and has requested that I analyze the data and present my key insights and findings.

I applied my SQL skills from the DSA Data Analysis class and solve both case scenariosas shared in the document [here]().

[Raw KMS data](https://drive.google.com/file/d/1BGndN0FlR9IHmV11S7HJ0cSmrcAhzseV/view?usp=drive_link)

[Analysed KMS SQL file](https://drive.google.com/file/d/1WKyWJailERYzxxZnqWSTNlj_IDJCyOCQ/view?usp=drive_link)

### Case scenario I
**No. 1**  Which product category had the highest sales?

**Ans: Technology-5,984,248.50 sales**

```SQL
select top 1 product_category,sum(sales) as totalsales
from [KMS Sql Case Study]
group by product_category
order by product_category desc
```

**No. 2** What are the Top 3 and Bottom 3 regions in terms of sales?

**Ans:**

**Top 3:**
- West,(3597,549.41)
- Ontario (3,063,212.60)
- Prarie (2837,304.60)
```SQL
select top 3 Region, sum(sales) as totalsales
from [KMS Sql Case Study]
group by Region
order by totalsales desc
```

**Bottom 3:**
- Nunavut	(116,376.47)
- Northwest Territories	(800,847.35)
- Yukon	(975,867.39)
```SQL
select top 3 Region, sum(sales) as totalsales
from [KMS Sql Case Study]
group by Region
order by totalsales ASC
```

**N0. 3:** What were the total sales of appliances in Ontario?

**Ans:** 202,346.84
```SQL
select sum(sales) as ontario_appliance_sales
from [KMS Sql Case Study]
where Product_Sub_Category = 'APPLIANCES' and province = 'ontario'
```

**No. 4:** Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers

**Ans:** Bottom 10 customers with lowest venue include:
- Jeremy Farry	(85.72)
- Natalie DeCherney	(125.90)
- Nicole Fjeld	(153.03)
- Katrina Edelman	(180.76)
- Dorothy Dickinson	(198.08)
- Christine Kargatis	(293.22)
- Eric Murdock	(343.33)
- Chris McAfee	(350.18)
- Rick Huthwaite	(415.82)
- Mark Hamilton	(450.99)
```SQL
select top 10 customer_name, sum(sales) as totalsales
from [KMS Sql Case Study]
group by Customer_Name
order by totalsales asc
```
*To get more info about these customers so I can give an informed advise, I ran the following query:*
```SQL
SELECT TOP 10 
    Customer_Name,
    MAX(Customer_Segment) AS Customer_Segment,
    MAX(Region) AS Region,
    SUM(Sales) AS TotalSales
FROM 
    [KMS Sql Case Study]
GROUP BY 
    Customer_Name
ORDER BY 
    TotalSales ASC
```
**My advise to increase revenue from these customers are:**
1. Understand why they purchase less (e.g., customer survey).
2. reduce shipping cost to these regions
3. Offer loyalty programs, bundles, or volume discounts.
4. Assign dedicated account reps for support and retention.
5. Market top-selling or complementary products to them.


**No. 5:** KMS incurred the most shipping cost using which shipping method?

**Ans:** Delivery Truck-519,71.94
```SQL
select top 1 ship_mode, sum(shipping_cost) as [total shipping cost]
from [KMS Sql Case Study]
group by ship_mode
order by [total shipping cost] desc
```

### Case Scenario II

**No. 6:** Who are the most valuable customers, and what products or services do they typically purchase?

**Ans:**

**Top 5 Most valuable customer in terms of sales**
1. Emily Phan	(117,124.43)
2. Deborah Brumfield (97,433.14)
3. Roy Skaria	(92,542.16)
4. Sylvia Foulston	(88,875.76)
5. Grant Carroll	(88,417.00)
```SQL
select top 5 customer_name, sum(sales) as [total sales]
from [KMS Sql Case Study]
group by Customer_Name
order by [total sales] desc
```
**Products or services that these customers purchase**
<img width="2560" height="1440" alt="Screenshot (166)" src="https://github.com/user-attachments/assets/59214c40-cfac-4faf-b0ba-16593ed8f98d" />

<img width="2560" height="1440" alt="Screenshot (167)" src="https://github.com/user-attachments/assets/c34dd2d2-8ce8-4ce3-b2d8-98fd2587b35a" />

```SQL
WITH TopCustomers AS (
    SELECT TOP 5 
        Customer_Name
    FROM 
        [KMS Sql Case Study]
    GROUP BY 
        Customer_Name
    ORDER BY 
        SUM(Sales) DESC
)
SELECT 
    Customer_Name, 
    Product_Sub_Category,
    COUNT(*) AS Num_Orders, 
    SUM(Sales) AS Total_Expenditure
FROM 
    [KMS Sql Case Study]
WHERE 
    Customer_Name IN (SELECT Customer_Name FROM TopCustomers)
GROUP BY 
    Customer_Name, Product_Sub_Category
ORDER BY 
    Customer_Name, Total_Expenditure DESC;
```

