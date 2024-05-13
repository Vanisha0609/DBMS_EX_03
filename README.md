# EXP No : 3                                                                              
# Date:19/03/2024

# AIM:           
To Study and Implement DML Commands.

# THEORY:
## 1. INSERT INTO: 
This is used to add records into a relation. 
These are three type of INSERT INTO queries which are as 

### a) Inserting a single record 
#### Syntax:
 INSERT INTO < relation/table name> (field_1,field_2……field_n)VALUES (data_1,data_2, ...... data_n);student(sno,sname,class,address)VALUES (1,’Ravi’,’M.Tech’,’Palakol’); 

 ### b) Inserting all records from another relation
#### Syntax:
 INSERT INTO relation_name_1 SELECT Field_1,field_2,field_n FROM relation_name_2 WHERE field_x=data;

### c) Inserting multiple records 
#### Syntax:
INSERT INTO relation_name field_1,field_2, ....field_n) VALUES (&data_1,&data_2,.......&data_n); 


## 2. UPDATE-SET-WHERE: 
This is used to update the content of a record in a relation. 
#### Syntax:
 SQL>UPDATE relation name SET Field_name1=data,field_name2=data, WHERE field_name=data; Example: SQL>UPDATE student SET sname = ‘kumar’ WHERE sno=1; 

## 3. DELETE-FROM: 
This is used to delete all the records of a relation but it will retain the structure of that relation. 
### a) DELETE-FROM: 
This is used to delete all the records of relation. 
#### Syntax:
DELETE FROM relation_name;
### b) DELETE -FROM-WHERE: 
This is used to delete a selected record from a relation. 
#### Syntax:
DELETE FROM relation_name WHERE condition; 

## 4. SELECT FROM: To display a set of fields for all records of relation
### Syntax: 
SELECT (column1,column2) FROM (Table Name)WHERE condition;

# MODULE:
## QUESTION 1:

<img src="https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/e19bd021-e761-43c2-a559-81538fcdd19f" width="900" height="250">


### QUERY:
```
SELECT salesman_id, name, city, commission
FROM salesman
WHERE city NOT IN ('Paris', 'Rome');
```
### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/6601fe35-9615-4212-9abd-9e2f9609881c)


## QUESTION 2:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/fa481c75-4454-4d72-9201-c2ff2bc23511)

### QUERY:
```
SELECT customer_id, cust_name, city, grade, salesman_id
FROM customer
WHERE city = 'New York' OR grade <= 100;
```
### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/5563649b-c5fc-421d-a1af-91f288e1c670)

## QUESTION 3:


### QUERY:
```
SELECT customer_id, cust_name, city, grade, salesman_id
FROM customer
WHERE city = 'New York' OR grade > 200;
```

### OUTPUT:


## QUESTION 4:

<img src="https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/4df48049-3ff5-4c24-bbe0-28c0bb770aca" width="800" height="400">


### QUERY:
```
SELECT categoryName, description
FROM categories
ORDER BY categoryName;
```
### OUTPUT:


## QUESTION 5:


### QUERY:
```
UPDATE products
SET reorder_lvl = 20
WHERE quantity < 10
AND category = 'Snacks';
```
### OUTPUT:

## QUESTION 6:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/80bb5433-00ee-4bec-9a1f-be11b3f93733)

### QUERY:
```
UPDATE employees
SET salary = CASE
    WHEN department_id = 40 THEN ROUND(salary * 1.25)
    WHEN department_id = 90 THEN ROUND(salary * 1.15)
    WHEN department_id = 110 THEN ROUND(salary * 1.10)
    ELSE salary
END
WHERE department_id IN (40, 90, 110);

```
### OUTPUT:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/8b16c54a-cb53-4708-89a4-605c83b7520d)

## QUESTION 7:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/934cd61f-61c6-41fa-924b-1b8d006c58e9)

### QUERY:
```
UPDATE products
SET quantity = quantity * 1.10;

```

### OUTPUT:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/8def8c67-5db9-457d-bfed-f6011dd3d6d1)

## QUESTION 8:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/fa2e2777-76a6-4dc7-a76a-08f1f53a9656)

### QUERY:
```
DELETE FROM customer
WHERE cust_city LIKE 'L%';

```

### OUTPUT:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/0d1b8e78-c395-4537-a2b1-47dcef3605c9)

## QUESTION 9:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/2762ce7b-92b3-4fac-ac87-4433a674eb25)

### QUERY:
```
DELETE FROM customer
WHERE OPENING_AMT BETWEEN 4000 AND 6000;
```
### OUTPUT:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/26871b8d-1a8f-4fc3-b4be-aff63da42bca)

## QUESTION 10:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/c583ec09-e93a-46df-968f-3f7b0450c38f)

### QUERY:
```
DELETE FROM doctors
WHERE Specialization IS NULL;
```
### OUTPUT:

![image](https://github.com/Mena-Rossini/DBMS_EX_03/assets/102855266/24173d96-c238-4def-a1c5-0c0bb1d16528)

# RESULT:
Thus,we studied and implemented some DML Commands.


