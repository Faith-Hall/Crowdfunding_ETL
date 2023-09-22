# Crowdfunding_ETL
---
## Group project 2: 
- Faith Hall
- Katy Yelle
- Matthew Byron
- Tristan Vazquez
---
## Project Overview 
> For the ETL mini project, you will work with a group to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.
---
## Repository Structure
  - Main Folder
    - .gitignore
    - README.md
  - Sub Folders
    - Starter_Files
      - ETL_Mini_Project_Starter_Code.ipynb
    - Code
      - Resources
        - category.csv
        - contacts.csv
        - crowdfunding.csv
        - subcategory.csv
      - ETL_Mini_Project_Group_7.ipynb
      - crowdfundingERD.png
      - crowdfunding_db_schema.sql
---
### <code style="color : red">Create the Category and Subcategory DataFrames</code>
- Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  - A "category" column that contains only the category titles

![Screenshot 2023-09-21 195314](https://github.com/Faith-Hall/Crowdfunding_ETL/assets/135525815/deebc022-b487-4f27-9378-3ac19b7f77ea)

- Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
  - A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  - A "subcategory" column that contains only the subcategory titles
  
![Screenshot 2023-09-21 195327](https://github.com/Faith-Hall/Crowdfunding_ETL/assets/135525815/86db5bfd-f9ee-4466-bc9d-38b6c3110263)

### <code style="color : red">Create the Campaign DataFrame</code>

### <code style="color : red">Create the Contacts DataFrame</code>

### <code style="color : red">Create the Crowdfunding Database</code>
- Create an ERD of the tables based on the four CSV files (category.csv,subcategory.csv, campaign.csv, and contacts.csv) using QuickDBD and saved as a png file.
- Save the database schema is as a Postgres file named 'crowdfunding_db_schema.sql'.
- Create a new Postgres database named crowdfunding_db.
- Verify table creation using a SELECT statement for each table.
- Import each CSV file into its corresponding SQL table.
- Verify table creation using a SELECT statement for each table. 
---
### Acknowledgements
We would like to thank our teaching staff:
- Hunter Hollis
- Sam Espe
- Randy Sendek


