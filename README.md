# Crowdfunding_ETL
---
## Group project 2: 
- Faith Hall
- Katy Yelle
- Matthew Byron
- Tristan Vazquez
---
## Project Overview 
##### For the ETL mini project, you will work with a group to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.
---
### Create the Category and Subcategory DataFrames
- Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  - A "category" column that contains only the category titles
```
crowdfunding_info_df[['category','subcategory']] = crowdfunding_info_df ["category & sub-category"].str.split('/' , expand=True)
crowdfunding_info_df.head()
```

### Create the Campaign DataFrame

### Create the Contacts DataFrame

### Create the Crowdfunding Database

---
### Acknowledgements



