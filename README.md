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
        - campaign.csv
        - category.csv
        - contacts.csv
        - crowdfunding.xlsx
        - subcategory.csv
      - ETL_Mini_Project_Group_7.ipynb
      - crowdfundingERD.png
      - crowdfunding_db_schema.sql
---
### <code style="color : red">Create the Category and Subcategory DataFrames</code>
- Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  - A "category" column that contains only the category titles

![Screenshot 2023-09-21 200814](https://github.com/Faith-Hall/Crowdfunding_ETL/assets/135525815/a7a7bec9-08b4-4c30-805d-5373457b427b)

- Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
  - A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  - A "subcategory" column that contains only the subcategory titles
  
![Screenshot 2023-09-21 200822](https://github.com/Faith-Hall/Crowdfunding_ETL/assets/135525815/4170456f-ada8-49f1-91f3-818ba0810519)
---
### <code style="color : red">Create the Campaign DataFrame</code>
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame:
- Create a copy of the crowdfunding_info_df DataFrame name campaign_df.
- Rename the blurb, launched_at, and deadline columns.
- Convert the goal and pledged columns to a `float` data type.
- Format the launched_date and end_date columns to datetime forma
- Merge the campaign_df with the category_df on the "category" column and the subcategory_df on the "subcategory" column.
- Drop unwanted columns
  
![Screenshot 2023-09-25 180838](https://github.com/Faith-Hall/Crowdfunding_ETL/assets/135525815/bb9862b6-26de-430c-99df-e471e7e0fd50)

---
### <code style="color : red">Create the Contacts DataFrame</code>
- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary, doing the following:
  - Extract the dictionary values from the keys by using a Python list comprehension.
  - Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and place each in a new column.
- Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.
---
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


