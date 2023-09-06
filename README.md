# crowdfunding_ETL

This repository is based on the ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. The second step after extraction is to transform the data, by creating four CSV files and using the CSV file data to create an ERD and a table schema. Finally, this data is uploaded into the CSV file data into a Postgres database.

## The instructions for this mini project are divided into the following subsections:

1. Create the Category and Subcategory DataFrames
2. Create the Campaign DataFrame
3. Create the Contacts DataFrame
4. Create the Crowdfunding Database



### 1. Create the Category and Subcategory DataFrames
a. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
 * A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
 * A "category" column that contains only the category titles

b. Export the category DataFrame as category.csv and save it to your GitHub repository.

c. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
 * A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
 * A "subcategory" column that contains only the subcategory titles

d. Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

### 2. Create the Campaign DataFrame
a. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
 * The "cf_id" column
 * The "contact_id" column
 * The "company_name" column
 * The "blurb" column, renamed to "description"
 * The "goal" column, converted to the float data type
 * The "pledged" column, converted to the float data type
 * The "outcome" column
 * The "backers_count" column
 * The "country" column
 * The "currency" column
 * The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
 * The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
 * The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
 * The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

b. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

### Create the Contacts DataFrame
a. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
 * Option 1: Use Python dictionary methods.
   * If you chose Option 1, complete the following steps:
   * Import the contacts.xlsx file into a DataFrame.
   * Iterate through the DataFrame, converting each row to a dictionary.
   * Iterate through each dictionary, doing the following:
     *   Extract the dictionary values from the keys by using a Python list comprehension.
     *   Add the values for each row to a new list.
  * Create a new DataFrame that contains the extracted data.
  * Split each "name" column value into a first and last name, and place each in a new column.
  * Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

### Create the Crowdfunding Database
a. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site..

b. Use the information from the ERD to create a table schema for each CSV file.

c. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

d. Create a new Postgres database, named crowdfunding_db.

e. Using the database schema, create the tables in the correct order to handle the foreign keys.

f. Verify the table creation by running a SELECT statement for each table.

g. Import each CSV file into its corresponding SQL table.

h. Verify that each table has the correct data by running a SELECT statement for each.






