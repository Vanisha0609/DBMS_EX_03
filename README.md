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
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/d58b73e6-291e-4a3e-96ac-aaa246285db6)


### QUERY:
```
SELECT customer_id, cust_name, city, grade, salesman_id
FROM customer
WHERE city = 'New York' OR grade > 200;
```

### OUTPUT:
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/62fe620a-99ce-4613-ba4f-6175845c515d)


## QUESTION 4:

<img src="https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/4df48049-3ff5-4c24-bbe0-28c0bb770aca" width="800" height="400">


### QUERY:
```
SELECT categoryName, description
FROM categories
ORDER BY categoryName;
```
### OUTPUT:
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/4eab895a-291d-479e-a5a1-460364190132)


## QUESTION 5:
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/ebab2f1c-fee1-4da1-bf7b-229d9fe1b6a8)


### QUERY:
```
UPDATE products
SET reorder_lvl = 20
WHERE quantity < 10
AND category = 'Snacks';
```
### OUTPUT:
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/7d149295-17bd-4b5e-8d6e-dbe46de01278)

## QUESTION 6:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/a49afbde-4e48-456f-a550-af3fac122360)

### QUERY:
```
UPDATE products
SET sell_price=sell_price*1.10
WHERE category='Bakery';
```
### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/2a38d0c9-6d9d-4ecc-b28a-df3651b547e0)

## QUESTION 7:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/289eac3c-33e8-41fe-b9ca-696a45471903)

### QUERY:
```
UPDATE employees
SET first_name = 'John'
WHERE department_id = 80
AND commission_pct < 0.35;
```

### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/b322b0f1-ca55-42c6-b441-34e293ddac0b)

## QUESTION 8:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/2419587d-c66c-48ad-9e4d-f6fb8c8b9256)

### QUERY:
```
DELETE FROM customer 
WHERE GRADE=2;
```

### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/f8af8b1f-9559-48eb-b4ca-fcee891f6c78)

## QUESTION 9:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/8670680f-7bb0-4516-be18-9a916901dde0)

### QUERY:
```
DELETE FROM customer
WHERE CUST_CITY  NOT IN ( 'New York')
AND OUTSTANDING_AMT >5000;
```
### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/3b95d3bb-f560-458b-b539-95c9851fe9d3)

## QUESTION 10:
![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/11a218c6-c829-4a65-b6a3-c57416aacb4d)


### QUERY:
```
DELETE FROM doctors
WHERE specialization IS NULL;
```
### OUTPUT:

![image](https://github.com/Vanisha0609/DBMS_EX_03/assets/119104009/68ed3a47-b94b-4c37-9541-00e3a518c1e5)

# RESULT:
Thus,we studied and implemented some DML Commands.


