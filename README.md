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
### <code style="color : red">Create the Category and Subcategory DataFrames</code>
- Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  - A "category" column that contains only the category titles
- Assign the category and subcategory values to category and subcategory columns.
```
crowdfunding_info_df[['category','subcategory']] = crowdfunding_info_df ["category & sub-category"].str.split('/' , expand=True)
crowdfunding_info_df.head()
```
- Get the unique categories and subcategories in separate lists.
```
categories = crowdfunding_info_df['category'].unique()
subcategories = crowdfunding_info_df['subcategory'].unique()
```
- Create numpy arrays from 1-9 for the categories and 1-24 for the subcategories.
 ```
category_ids = np.arange(1, 10)
subcategory_ids = np.arange(1, 25)
```
- Use a list comprehension to add "cat" to each category_id.
```
cat_ids = [f"cat{category_id}" for category_id in category_ids]
```
- Use a list comprehension to add "subcat" to each subcategory_id.
```   
scat_ids = [f"subcat{subcategory_ids}" for subcategory_ids in subcategory_ids]
```
- Create a category DataFrame with the category_id array as the category_id and categories list as the category name.
```
category_dictonary = {'category_id': cat_ids , 'category': categories}
category_df = pd.DataFrame(category_dictonary)
```
- Create a category DataFrame with the subcategory_id array as the subcategory_id and subcategories list as the subcategory name. 
```
subcategory_dictonary = {'subcategory_id': scat_ids , 'subcategory': subcategories}
subcategory_df = pd.DataFrame(subcategory_dictonary)
```
- Export categories_df and subcategories_df as CSV files.
```
category_df.to_csv("Resources/category.csv", index=False)

subcategory_df.to_csv("Resources/subcategory.csv", index=False)
```
### Create the Campaign DataFrame

### Create the Contacts DataFrame

### Create the Crowdfunding Database

---
### Acknowledgements



