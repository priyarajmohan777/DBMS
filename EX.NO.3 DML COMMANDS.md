# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharini',2500,500,30000,'30-June-81','intern',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```
UPDATE manager
SET salary = salary * 1.1
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/38223d6b-dff8-47f4-aaad-2b5a1ee4a664)

### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
```
DELETE FROM manager
WHERE salary < 2750;
```

### OUTPUT:

![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/3d6169d4-3168-40f2-9ecc-eb65ed15370b)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
```
SELECT ename AS "Name", salary * 12 AS "Annual Salary"
FROM manager;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/53d5ccac-cb8f-43ce-ad48-2f2edb808e60)

### Q5)	List the names of Clerks from emp table.


### QUERY:
```
SELECT ename
FROM manager
WHERE designation = 'clerk';
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/9a53d561-e8b6-4c25-98a4-05c3d85c5314)



### Q6)	List the names of employee who are not Managers.


### QUERY:
```
SELECT ename
FROM manager
WHERE designation <> 'manager';
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/035d4a9e-cbb3-4f0b-8f53-b05fc8aaccd6)


### Q7)	List the names of employees not eligible for commission.


### QUERY:
```
SELECT ename
FROM manager
WHERE commission = 0 OR commission IS NULL;
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/ed2c07d0-9825-4df9-af95-307be7eb1fbd)


### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
```
SELECT ename
FROM manager
WHERE ename LIKE 's%' OR ename LIKE '%s';
```

### OUTPUT:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/b3e4062b-b37d-4fa6-b3dd-7a4efe4000a2)


### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
```
SELECT ename, designation AS job, deptno, Hiredate
FROM manager
ORDER BY Hiredate ASC;
```

### OUTPUT:


### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:


### OUTPUT:


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:


### OUTPUT:


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:


### OUTPUT:

### Q13) Find number of rows in the table EMP

### QUERY:


### OUTPUT:


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:


### OUTPUT:


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:


### OUTPUT:


## RESULT :
Thus the basic DML commands are executed.
