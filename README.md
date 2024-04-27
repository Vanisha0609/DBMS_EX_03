# EXP No.3      &NSBP                                                                       Date:19/03/2024

AIM:          
 
To Study and Implement DML Commands.

THEORY:

1. INSERT INTO: This is used to add records into a relation. 

These are three type of INSERT INTO queries which are as 

a) Inserting a single record 

Syntax:
 INSERT INTO < relation/table name> (field_1,field_2……field_n)VALUES (data_1,data_2, ...... data_n);student(sno,sname,class,address)VALUES (1,’Ravi’,’M.Tech’,’Palakol’); 

 b) Inserting all records from another relation

Syntax:
 INSERT INTO relation_name_1 SELECT Field_1,field_2,field_n FROM relation_name_2 WHERE field_x=data;

 c) Inserting multiple records 

Syntax: INSERT INTO relation_name field_1,field_2, ....field_n) VALUES (&data_1,&data_2,.......&data_n); 


2. UPDATE-SET-WHERE: 
This is used to update the content of a record in a relation. 

Syntax:
 SQL>UPDATE relation name SET Field_name1=data,field_name2=data, WHERE field_name=data; Example: SQL>UPDATE student SET sname = ‘kumar’ WHERE sno=1; 


3. DELETE-FROM: This is used to delete all the records of a relation but it will retain the structure of that relation. 

a) DELETE-FROM: This is used to delete all the records of relation. 
Syntax: DELETE FROM relation_name;

b) DELETE -FROM-WHERE: This is used to delete a selected record from a relation. 
Syntax:DELETE FROM relation_name WHERE condition; 


4)SELECT FROM: To display a set of fields for all records of relation

Syntax: 
SELECT (column1,column2) FROM (Table Name)WHERE condition;
