# Introduction to Databases with SQLite

## Dataset Details

### Hospital Dataset 1: Mount Sinai Queens
This dataset is the chargemaster data from the Mount Sinai Queens website, detailing charge codes, descriptions and rates.

### Hospital Dataset 2: New York Presbyterian
This dataset is the chargemaster data from New York Presbyterian Hospital, detailing charge codes, descriptions, hospital rates and insurance payout rates.

## Eploratory Data Analysis (EDA) 
<b> The EDA Process was the same for both datasets

### Data Cleaning
1.  After data import, the shape and first ten rows were requested to being visualizing data
2. Columns were viewed to understand the data better and visualize special characters
3. Empty columns were dropped
4. Rows with extensive numbers of missing values were dropped
5. Duplicate rows dropped
6. Columns were renamed to remove special characters
7. Based on the type of data included, some columns were converted to string/float/int. Any values that prevented this conversion were dropped.
8. The cleaned dataset was exported to .csv and used in the rest of the code

### EDA Process
1. Use the describe function to display count, mean, standard deviation, min, max and quartiles
2. Calculate mean, median, mode, range, variance and standard deviation for each float or int columns
3. Display data distribution using the Figure function
4. For the string columns, use the value counts function to sum the number of times a value is used per column
   
## SQLite Database
### Manual table creation
1. Create the database (health.db) using conn and defining c
2. Create the table (msqCharges7), columns(Charge_description, Department_name, Rate_Charged, PaidClaim, LostRevenue) and values (test, text, treal, real, real) using c.execute and conn.commit
3. Use c.execute to confirm that the table was added to the new database
4. Use INSERT INTO to add values into the table created (Mount Sinai Queens, Outpatient Surgery, 10000, 5000, 5000)
5. Use c.execute(sql_query) and conn.commit to add the values to the table
6. Create a variable to store the updated table, execute, and print the values in the table
7. Use the read sql and to sql functions to store the table in sql
8. Use the read sql query to print the final table
### Automatic table creation
1. Import CSV dataset using read csv function
2. Convert the database to sql using to_sql
3. Using query and read sql, print the sql table
