# Spar_Nord_Bank_Atm

The overall task in this project will be to build a batch ETL pipeline to read transactional data from RDS, transform and load it into target dimensions and facts on Redshift Data Mart(Schema).

Once the data is loaded into Redshift, you would have to write the analytical queries discussed above.

We have data from more than 100 ATMs across Denmark. Data is captured for every transaction including, card type, location, date, time, ATM type, etc.

Also, the transaction amount field in the data set was added separately using a random function for the analysis purpose.

Spar Nord Bank has also built a dimensional model datastore (ATM Data Mart) on this ATM transaction data to understand the ATM usage pattern. This exact schema(target schema) of this Data Mart will be provided to you for the sake of this project. Basically, this will be the schema according to which we will be creating tables in Redshift.

Broadly we will be performing the following task-

> Extracting the transactional data from a given MySQL RDS server to HDFS(EC2) instance using Sqoop.

> Transforming the transactional data according to the given target schema using PySpark.

> This transformed data is to be loaded to an S3 bucket.

> Creating the Redshift tables according to the given schema.

> Loading the data from Amazon S3 to Redshift tables.

> Performing the following analysis queries:
```
  1) Top 10 ATMs where most transactions are in the ’inactive’ state
  
  2)Number of ATM failures corresponding to the different weather conditions recorded at the time of the transactions
  
  3)Top 10 ATMs with the most number of transactions throughout the year
  
  4)Number of overall ATM transactions going inactive per month for each month
  
  5)Top 10 ATMs with the highest total amount withdrawn throughout the year
  
  6) Number of failed ATM transactions across various card types
  
  7)Top 10 records with the number of transactions ordered by the ATM_number, ATM_manufacturer, location, weekend_flag and then total_transaction_count, on weekdays and on weekends throughout the year
  
  8)Most active day in each ATMs from location "Vejgaard"
```
