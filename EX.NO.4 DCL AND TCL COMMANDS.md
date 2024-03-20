# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
CREATE TABLE employee (
    employee_id INT,
    name VARCHAR(50),
    address VARCHAR(50)
);


### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/8f89c2f6-64a0-4c46-b5b0-93bf368e62b5)

### Q2) Insert three rows into emploee table 

### QUERY:
insert into employee(employee_id,name,address)values(1,'Dhanu','123 Main st');
insert into employee(employee_id,name,address)values(2,'Abi','456 Oakst');
insert into employee(employee_id,name,address)values(3,'Yazhini','345 Oak st');

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/59ab9139-b8dd-4f7e-b00a-2d5cea4c20be)

### Q3) Start the transaction and create a save point s1.

### QUERY:
EXEC SAVEPOINT S1;

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/50088cb0-2901-4a09-87a7-19780566349c)

### Q4) Perform insertion into employee table.

### QUERY:
INSERT INTO employee (employee_id, name, address) VALUES (5, 'Yuri', '567 Elm St');

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/958fac29-38fb-4955-b2eb-832a3592a9d7)


### Q6)	Display the employee table and create a save point s2 .


### QUERY:
SELECT * FROM employee;
SAVEPOINT s2;

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/81b987bd-9f2e-4f56-b24f-b1b505cbd976)


### Q7)	Perform updation on any one of the row.


### QUERY:
UPDATE employee
SET address = '123 Maple St'
WHERE employee_id = 2;



### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/0a82bb48-1560-4a52-8789-c527c2ba4233)



### Q8) Display the employee table and rollback to  save point s2 


### QUERY:
SELECT * FROM employee;
ROLLBACK TO SAVEPOINT s2;

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/91377c70-cd56-465a-8337-36e4d0d2ff08)


### Q9) Display the employee table and commit the changes; 


### QUERY:
SELECT * FROM employee;
COMMIT;

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/8b723522-9cda-42b0-aaaf-a7346b7438c8)


### Q10) Rollback to save point s1;


### QUERY:


### OUTPUT:


### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:


### OUTPUT:


### Q12) Check the user access and display the result 


### QUERY:


### OUTPUT:

### Q13) Revoke the privillages.

### QUERY:


### OUTPUT:


## RESULT :
Thus the basic TCL and DCL commands are executed.
