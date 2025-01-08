# Crowdfunding_ETL
This project demonstrates the ability to build an ETL pipeline using Python, Pandas, and Python dictionary methods to look at crowdfunding data. After processing the data and creating four CSV files, I created a schema to upload the CSV data into a Postgres database.

# Repository Structure
**ETL_Pipeline:**
  + **ETL_Mini_ProjectCNunez:** File containing code to transform original CSV files into four, cleaned CSV files.
  + **crowdfunding_db_scheme.sql** SQL code generated by using the QuickDBD tool, representing the database schema.
**Resources Folder:** Contains the necessary CSV files for creating the new CSV files.

  +**Output:** Contains the four new CSV files created.
  
# Instructions to Run the Files
**1. Set Up the Database and Tables:**

Open and Execute the Schema Script:
  + Open PGAdmin and create a database called 'crowdfunding_db'
  + Open the crowdfunding_db_scheme.sql file in the new 'crowdfunding_db'
    +To ensure code can be re-run, use the following drop statements before the schema code:
    
      +DROP TABLE IF EXISTS campaign;
      +DROP TABLE IF EXISTS category;
      +DROP TABLE If EXISTS contacts;
      +DROP TABLE IF EXISTS subcategory;
    
  + Execute the entire script to create the tables

**2. Import the Data:**

After executing the schema, import the CSV data into the database tables in the following order:
1. **category**
2. **subcategory**
3. **contacts**
4. **campaign**

You can import the data using the Import/Export feature in PGAdmin

**3. Run SELECT Statements:**

Open a new query and run the following SELECT statements to ensure the tables function properly:

SELECT * FROM category;

SELECT * FROM subcategory;

SELECT * FROM contacts;

SELECT * FROM campaign
