# Grocery - Report

- Use AWS cloud platform to store data, then use Snowflake to get data from AWS. Then connect to Power BI to make reports.
- The aim this report is to evaluate and understand the overall sales performance of the grocery store chain, while also identifying the key factors influencing revenue and the number of items sold.
- Help managers make data-driven decisions to optimize sales strategies, product portfolio management, and store operations.

## Dataset 

Reference documents and datasets: [Amazing Real Time Power BI Project](https://www.youtube.com/watch?v=mmxVCFceQgU&list=PLO9LeSU_vHCWUvkE1FrGeNxSve7YtJrYl&index=2)

### Dataset Description

- Grocery dataset has collected sales data from the year 2011. Where the dataset consists of 12 attributes like Item Fat Content, Item Identifier, Item Type, Item Visibility, Item Weight, Outlet Identifier, Outlet Establishment Year, Outlet Location Type, Outlet Size, Outlet Type, Sales and Rating. 
- Mini project.

### Data Detail

The data has 8523 rows of 12 variables.

- Variable - Details
  + Item_Fat_Content - Whether the product is low fat or not
  + Item_Identifier - Unique product ID
  + Item_Type - The category to which the product belongs
  + Item_Visibility - The % of total display area of all products in a store allocated to the particular product
  + Item_Weight - Weight of product
  + Outlet_Identifier - Unique store ID
  + Outlet_Establishment_Year - The year in which store was established
  + Outlet_Location_Type - The type of city in which the store is located
  + Outlet_Size - The size of the store in terms of ground area covered
  + Outlet_Type- Whether the outlet is just a grocery store or some sort of supermarket
  + Sales - Sales of the product.
  + Rating - Customer reviews of store products or services (1 - 5).

## Setup

### AWS

1. Create S3 Bucket on AWS & Loading Data
- Create Buckets: powerbi.project.s1
<img width="1394" height="683" alt="image" src="https://github.com/user-attachments/assets/7a40a93b-50ae-4bc4-b39d-a7e3fb52b315" />

- Loading Data into bucket:
<img width="1861" height="540" alt="image" src="https://github.com/user-attachments/assets/50c86b26-0f18-4c17-9747-9cb21472c67a" />

2. 
### Snowflake

### Connect to Power BI

