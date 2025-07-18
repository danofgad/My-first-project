# Kultra Mega Stores Inventory
#### Kultra Mega Stores (KMS), headquartered in Lagos, specialises in office supplies and furniture. Its customer base includes individual consumers, small businesses (retail), and large corporate clients (wholesale) across Lagos, Nigeria.
#### I have been engaged as a Business Intelligence Analyst to support the Abuja division ofKMS. The Business Manager has shared an Excel file containing order data from 2009 to 2012 and has requested that I analyze the data and present my key insights and findings.

I applied my SQL skills from the DSA Data Analysis class and solve both case scenariosas shared in the document [here]().

[Raw KMS data](https://drive.google.com/file/d/1BGndN0FlR9IHmV11S7HJ0cSmrcAhzseV/view?usp=drive_link)

[Analysed KMS SQL file](https://drive.google.com/file/d/1WKyWJailERYzxxZnqWSTNlj_IDJCyOCQ/view?usp=drive_link)

### Case scenario I
**No. 1**  Which product category had the highest sales?

**Ans: Technology-5984248.50 sales**

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
- Nunavut	(116376.47)
- Northwest Territories	(800847.35)
- Yukon	(975867.39)
```SQL
select top 3 Region, sum(sales) as totalsales
from [KMS Sql Case Study]
group by Region
order by totalsales ASC
```

