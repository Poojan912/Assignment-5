# Join Size Estimator

The join size estimatorl designed to estimate and analyze the size of joins between two tables in a relational database. It provides metrics like estimated join size, actual join size, and estimation error.

## Team Members

- Jainil Amitkumar Patel-JP828435
- Poojan Rasiklal Akhani- PA716942
- Jainish Nikul Shah- JS451591

## Prerequisites

Before you run the Database Join Analyzer, make sure you have the following installed:
- Java JDK 8 or higher
- Access to a SQL database with JDBC support

## Setup

To run the Join size Estimator command from the terminal:
--bash
java -cp "path/to/jdbc/driver.jar:path/to/project/bin" App.java <databaseURL> <table1> <table2>

The databse URL must have username and password
jdbc:postgresql://localhost:5432/pa71?user=<username>&password=<password> table1 table2

## Testing

The tables have at least one joinable column each, with some overlapping data to validate join calculations.
Then replace the placeholders with actual column names you are joining on 
Make tis changes in App.java file 

String joinColumnTable1 = "id"; // Replace with actual join column of table1

String joinColumnTable2 = "id"; // Replace with actual foreign key column of table2 in table1

The above example shows that we join on table1.id=table2.id 
e.g When we join student and takes on id the names of both should be 'id' as the attributes name in both table is 'id'

## Example for student join takes:
arguments:
![image](https://github.com/Poojan912/Assignment-5-Software/assets/104124712/49c78c2e-2ab0-4b3f-9b5d-6f5c46ab2e1f)

Successful execution:
![image](https://github.com/Poojan912/Assignment-5-Software/assets/104124712/1d55e3dc-8968-4e91-be57-df6b25d05874)


![image](https://github.com/Poojan912/Assignment-5-Software/assets/104124712/4c5e3f9c-3f1d-4940-bbc0-aa785413eb97)


## Logic:
If we assume that every tuple t in R produces tuples in R S, the number
of tuples in R ⨝ S is estimated to be: (nr x ns)/V(A,s) 
If the reverse is true, the estimate obtained will be: (nr x ns)/V(A,r) 
The lower of these two estimates is probably the more accurate one.




