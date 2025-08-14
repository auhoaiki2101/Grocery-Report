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

2. Creating the Role
- Select trusted entity:

<img width="1614" height="756" alt="image" src="https://github.com/user-attachments/assets/f0c46c80-f4ac-44cf-9fa3-3ca8a2f906dd" />

- Add permissions:

<img width="1523" height="502" alt="image" src="https://github.com/user-attachments/assets/a447dc62-79d7-4913-89a5-2c1249ae2772" />

- Name, review, and create:

<img width="1517" height="705" alt="image" src="https://github.com/user-attachments/assets/183773a5-9c0e-4208-83ad-40ae15015d1e" />

### Snowflake

1. Creating the Integration Object & Updating the Trust Policy.
- Creating the Integration Object.

<img width="761" height="317" alt="image" src="https://github.com/user-attachments/assets/da162d8f-e6d8-4844-9ea8-7e49ec58ebd0" />

- Run **desc integration PBI_Integration;**:

<img width="1264" height="382" alt="image" src="https://github.com/user-attachments/assets/79620d3e-d674-4cf5-99a5-144f9e3e016c" />

- Copy **'proprety_value'** for **STOAGE_AWS_IAM_USER_ARN** and **STORAGE_AWS_EXTERNAL_ID**:

<img width="1264" height="382" alt="image" src="https://github.com/user-attachments/assets/df3562b9-8290-49cb-9eb0-d6a4ee432c7b" />

<img width="1252" height="371" alt="image" src="https://github.com/user-attachments/assets/18eca092-3c8a-429f-949c-ca7ff02aa932" />

- Paste it in **Trust Policy** on **AWS IAM** and **Save**:

<img width="944" height="576" alt="image" src="https://github.com/user-attachments/assets/b6980d00-54ba-4723-bacf-1c817f64ad72" />

2. Loading Data into Snowflake.

- Create Database, schema and table:

<img width="394" height="374" alt="image" src="https://github.com/user-attachments/assets/a477b02c-541a-4fe7-98aa-51adfb85b9c1" />

- Create stage:

<img width="408" height="81" alt="image" src="https://github.com/user-attachments/assets/998a0acb-f074-4c9b-b832-914d75679885" />

- Copy data into PBI_Dataset:

<img width="1199" height="263" alt="image" src="https://github.com/user-attachments/assets/7557faae-1fe8-446a-b6ca-da97c923af6a" />

- Show dataset:

<img width="1247" height="784" alt="image" src="https://github.com/user-attachments/assets/8cbcd661-aa37-4b5f-afb4-d1f77f34bf54" />

### Connect to Power BI.
- Find Snowflake on PowerBI:

<img width="1458" height="849" alt="image" src="https://github.com/user-attachments/assets/f679f3fd-f1c9-46ef-be98-6564b9491a4b" />

- Copy **Server URL**:

<img width="889" height="633" alt="image" src="https://github.com/user-attachments/assets/3be46631-bd20-47d2-bc65-0e42001dc9a3" />

- Paste in **Server name** on Snowflake and choice your **Warehouse**:

<img width="711" height="285" alt="image" src="https://github.com/user-attachments/assets/9c9bc600-b94a-43e8-8d6e-a19e04f84d10" />

- Sign in **username** and **password** on this:

<img width="698" height="251" alt="image" src="https://github.com/user-attachments/assets/dede2335-58d3-4bed-91ab-8c5c7cb0d009" />

- Find your dataset and **Load**:

<img width="884" height="703" alt="image" src="https://github.com/user-attachments/assets/35800fe5-3afb-455e-993a-9b14e51ae9f1" />

- Complete:

<img width="1910" height="862" alt="image" src="https://github.com/user-attachments/assets/36c2c7da-29b9-4dad-b5ab-9c2bc6d816dc" />

