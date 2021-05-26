# ETL_challenge

## Google Store Ecommerce Data + Fake Retail Data: ##

Actual order level data from 2017 on the Google Store + Fake companion data

![Retail photo](https://github.com/danyelledoucette/ETL_challenge/blob/main/Images/retail.jpg)

**Extract**
- pull data from .csv files (KEY_SKU, Marketing_Spend, Online, Retail)
- read into pandas dataframes

**Transform**
- rename columns for consistency across dataframes
- re-formatted dates for consistency across dataframes
- dropped missing values
- merge retail to key_sku -> sku_retail_join
- merge sku_retail_join to online -> retail_online_join
- rename columns, drop unncessary columns -> new_retail_online
- merge to create final_join dataframe; merge new_retail_online to marketing
- set index to invoice_date

**Load**
- connect to pgAdmin database
- read dataframes to database

**ETL Report**
- calculate time elapsed for each df, row count for each df, errors for each df
- create df for each of the above variables
- export to .html file

**ETL Requirements**
- flow through .xlsx file
- four sheets containing information on how dataframes were assembled (extraction and transformation)
