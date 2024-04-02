# Ex. No: 8 PL/SQL program using Cursor 
### DATE: 
### AIM: To create PL/SQL program to display the customer table 

### Steps:
1. Declare the variable  in Declare section.
2. Fetch the variable with datatype similar to data type in cursor 
3. Create a cursor to select all rows from customers table.
4. Display the result 
5. End the begin section.

### Program:
```
DECLARE
    v_id CUSTOMER.CUSTOMER_ID%TYPE;
    v_name CUSTOMER.NAME%TYPE;
    v_email CUSTOMER.EMAIL%TYPE;

    CURSOR c_cursor IS
        SELECT CUSTOMER_ID, NAME, EMAIL
        FROM CUSTOMER;
BEGIN
    OPEN c_cursor;
    LOOP
        FETCH c_cursor INTO v_id, v_name, v_email;
        EXIT WHEN c_cursor%NOTFOUND;
        
        DBMS_OUTPUT.PUT_LINE('ID: ' || v_id || ', Name: ' || v_name || ', Email: ' || v_email);
    END LOOP;
    CLOSE c_cursor;
END;

```

### Output:
![image](https://github.com/priyarajmohan777/DBMS/assets/119475942/81f95e0c-61ca-4054-88de-35a31b1d922b)


### Result:
Thust the program was performed sucessfully.
