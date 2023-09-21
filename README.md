# Crowdfunding_ETL
---
## Group project 2: 
- Faith Hall
- Katy Yelle
- Matthew Byron
- Tristan Vazquez
---
## Project Overview 
#### For the ETL mini project, you will work with a group to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.
---
<details>
<summary>Create the Category and Subcategory DataFrames</summary>
<br>
After reading the crowdfunding data into a Pandas DataFrame and looking at the columns we needed to assign the category & subcategory to category and subcategory columns.
```
crowdfunding_info_df[['category','subcategory']] = crowdfunding_info_df ["category & sub-category"].str.split('/' , expand=True)
```
Then we got the unique categories and subcategories in separate lists.
```
categories = crowdfunding_info_df['category'].unique()
subcategories = crowdfunding_info_df['subcategory'].unique()
```
  
</details>

<details>
<summary>Create the Campaign DataFrame</summary>
<br>
(YOUR INFO HERE)
</details>

<details>
<summary>Create the Contacts DataFrame</summary>
<br>
(YOUR INFO HERE)
</details>

<details>
<summary>Create the Crowdfunding Database</summary>
<br>
(YOUR INFO HERE)
</details>
---
### Acknowledgements



