# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```
CREATE TABLE EMPLOYEE (
    EMPLOYEE_ID INT PRIMARY KEY,
    NAME VARCHAR(50),
    DEPARTMENT VARCHAR(50),
    SALARY DECIMAL(10, 2)
);
INSERT INTO EMPLOYEE (EMPLOYEE_ID, NAME, DEPARTMENT, SALARY) VALUES (1, 'John Doe', 'Engineering', 60000.00);
INSERT INTO EMPLOYEE (EMPLOYEE_ID, NAME, DEPARTMENT, SALARY) VALUES (2, 'Jane Smith', 'Marketing', 55000.00);

```
### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/eab32ace-c26e-4770-9a7f-26b6400d05d3)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/e62ca260-db64-43b6-b236-d398e9819184)


### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/dfb3483f-734e-47f8-a712-57c99e41bc15)


### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/dc69b9e9-9c44-4460-a1b3-e2c183d75d8e)



### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE TABLE SUPPLIER (
    ID INT PRIMARY KEY,
    NAME VARCHAR(50),
    ADDRESS VARCHAR(100),
    PHONE VARCHAR(20)
);

CREATE SEQUENCE S2 START WITH 1 INCREMENT BY 1;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/4b8e8057-9e12-4810-80b9-f15ca2007207)


### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO SUPPLIER (ID, NAME, ADDRESS, PHONE)
VALUES (S2.NEXTVAL, 'Supplier 1', '123 Main St', '123-456-7890');

INSERT INTO SUPPLIER (ID, NAME, ADDRESS, PHONE)
VALUES (S2.NEXTVAL, 'Supplier 2', '456 Elm St', '987-654-3210');
```

### OUTPUT:

![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/2468a818-019c-4a30-be75-0113504a13ce)

### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```

### OUTPUT:

![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/ff17b972-87f4-462f-9739-ea5ba290cb8e)

## RESULT :
### Thus the sequence and synonym created and used in SQL.
