# Amazon Product Review Analysis
### Company Overview:
#### I am working as a Junior Data Analyst at RetailTech Insights, a company that provides e-commerce analytics solutions to sellers on platforms like Amazon. My team has been tasked with analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.
### Dataset Description:
#### The dataset contains information scraped from Amazon product pages, including:
1. Product details: name, category, price, discount, and ratings
2. Customer engagement: user reviews, titles, and content
3. Each row represents a unique product, with aggregated reviewer data stored as comma-separated values
- Total Records: 1,465 rows
- TotalFields: 16 columns

[Raw Amazon Products Data](https://docs.google.com/spreadsheets/d/1BGDJuiR3eJNkdvl3DBTvwCM-M1iCRkE_/edit?usp=drive_link&ouid=101004108638642852403&rtpof=true&sd=true)

**Analysed Amazon spreedsheet containing: Cleaned data, Calculated columns, Pivot tables and Dashboard** [Here](https://docs.google.com/spreadsheets/d/1PFwGk3agFjWzSYyHFDad4vZqFzJxZZyJ/edit?usp=drive_link&ouid=101004108638642852403&rtpof=true&sd=true)

## Analysis Tasks:
Use pivot tables and calculated columns where necessary to answer the following:

**No 1:** What is the average discount percentage by product category?
<img width="394" height="230" alt="image" src="https://github.com/user-attachments/assets/6cef29a0-bad7-4c5b-b88d-535e197c9d71" />

**N0. 2:** How many products are listed under each category?
<img width="366" height="226" alt="image" src="https://github.com/user-attachments/assets/eeac40ba-9fee-44f1-b47e-8ed4afbe72ea" />

**No. 3:** What is the total number of reviews per category?
<img width="413" height="227" alt="image" src="https://github.com/user-attachments/assets/8fefa103-fdfe-4c97-bd9a-85158fc42368" />

**No. 4:** Which products have the highest average ratings?
<img width="398" height="227" alt="image" src="https://github.com/user-attachments/assets/2d4ec9dc-bae8-436f-bc40-92dcff00b1ce" />
<img width="615" height="241" alt="image" src="https://github.com/user-attachments/assets/06da68fe-1b5e-4669-8ae6-04145947f415" />


**No. 5:** What is the average actual price vs the discounted price by category?
<img width="583" height="228" alt="image" src="https://github.com/user-attachments/assets/c6caf3a6-407f-4448-8ee9-9d6bc4a58c6b" />

**No. 6:** Which products have the highest number of reviews?

**Ans:**

*Using filters and sort on the cleaned data, the **Top 5** products with the highest number of reviews include:*
1. AmazonBasics Flexible Premium HDMI Cable (Black, 4K@60Hz, 18Gbps), 3-Foot
2. Amazon Basics High-Speed HDMI Cable, 6 Feet - Supports Ethernet, 3D, 4K video,Black
3. Amazon Basics High-Speed HDMI Cable, 6 Feet (2-Pack),Black
4. boAt Bassheads 100 in Ear Wired Earphones with Mic(Taffy Pink)
5. boAt Bassheads 100 in Ear Wired Earphones with Mic(Furious Red)

**No. 7:** How many products have a discount of 50% or more?

**Ans:** Using filters in the cleaned dataset, the number of products with 50% or more discount is **751**

**No. 8:** What is the distribution of product ratings (e.g., how many products are rated 3.0,
4.0, etc.)?
<img width="412" height="529" alt="image" src="https://github.com/user-attachments/assets/9428066b-0fb8-467b-b730-26be25afdd53" />
<img width="437" height="134" alt="image" src="https://github.com/user-attachments/assets/55084267-d60b-420a-a91b-645c34c20416" />

**N0. 9:** What is the total potential revenue (actual_price × rating_count) by category?
<img width="665" height="390" alt="image" src="https://github.com/user-attachments/assets/7b746e23-9967-4a9e-a351-2bf85fcfff44" />

**No. 10:** What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
<img width="780" height="184" alt="image" src="https://github.com/user-attachments/assets/4778c404-0890-497f-b43c-5a5b8628c1b3" />

**No 11:** How does the rating relate to the level of discount?
<img width="533" height="461" alt="image" src="https://github.com/user-attachments/assets/b2ff32ae-308d-47df-953b-e2b6d32fecef" />

The relationship between rating and discount is weak or not strongly predictive because there is no clear cut pattern of direct or inverse proportionality as the top 2 products with the highest discount have very low rating while the highest rated products have close to the highest discount percentage.

**No 12:** How many products have fewer than 1,000 reviews?

**Ans:** Using filters in the cleaned dataset, the number of products with <1000 reviews is **326**.

**No. 13:** Which categories have products with the highest discounts?
<img width="629" height="360" alt="image" src="https://github.com/user-attachments/assets/e53555ee-cc59-4d3a-baf0-c2793308385e" />

**No. 14:** Identify the top 5 products in terms of rating and number of reviews combined.

**Ans:**

Using filters and sort on the 'Rating x Review' column in the cleaned dataset, the **Top 5** products in terms of rating and number of reviews combined are:
1. Amazon Basics High-Speed HDMI Cable, 6 Feet (2-Pack),Black
2. AmazonBasics Flexible Premium HDMI Cable (Black, 4K@60Hz, 18Gbps), 3-Foot
3. Amazon Basics High-Speed HDMI Cable, 6 Feet - Supports Ethernet, 3D, 4K video,Black
4. boAt Bassheads 100 in Ear Wired Earphones with Mic(Taffy Pink)
5. boAt Bassheads 100 in Ear Wired Earphones with Mic(Furious Red)

## DASHBOARD
**Click [here](https://docs.google.com/spreadsheets/d/1PFwGk3agFjWzSYyHFDad4vZqFzJxZZyJ/edit?usp=drive_link&ouid=101004108638642852403&rtpof=true&sd=true) to see dashboard**

Below are some pictures of the dashboard:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/16a0fca5-ff6d-41e8-bbe5-e5980dcd1905" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ae585133-cdc0-4cb2-b772-d63deb18a7d8" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/24dc2b33-36f2-4f3a-bc13-e843b371a842" />



