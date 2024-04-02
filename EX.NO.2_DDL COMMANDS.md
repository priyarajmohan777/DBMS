# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:

### 1) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
CREATE TABLE student (
    RegisterNumber INT,
    Name VARCHAR(100),
    Age INT,
    Address VARCHAR(255),
    PhoneNumber INT
);
```
### OUTPUT:
![Screenshot 2024-03-20 110343](https://github.com/priyarajmohan777/DBMS/assets/119475942/52854c0e-57f0-4bc8-a45f-11e5929010f3)

### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
ALTER TABLE student
ADD COLUMN department VARCHAR(100);
```
### OUTPUT:
![Screenshot 2024-03-20 110343](https://github.com/priyarajmohan777/DBMS/assets/119475942/cd2e81ef-e5e4-41ba-a112-e18fc75c4470)

### 3) Rename the student table to mystudent

### SQL QUERY: 
```
ALTER table students rename to mystudent;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/c39f3185-669d-49b6-a3bc-287d59324dfe)

### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
TRUNCATE table mystudent;
```
### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/055b2662-8efd-45b9-a194-347ad4ba34a9)

### 5) Drop the mystudent table
 
### SQL QUERY: 
```
DROP table mystudent;
```
### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/101ced66-1947-4868-9763-0b83b38a01f4)








## Result:
         Thus the basic DDL commands in SQL are executed. 


