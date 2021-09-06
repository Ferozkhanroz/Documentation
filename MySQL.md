# MySQL

## DDL

**DEFINITION :** *DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.*

`COMMANDS:`<br>
> - CREATE 
> - DROP
> - ALTER
> - TRUNCATE

#### **CREATE DATABASE :**

>**SYNTAX :** <br>  CREATE DATABASE db_name;

`EXAMPLE :`
```
CREATE DATABASE hrmanagement;
```
`USE DATABASE : `
>**SYNTAX :** <br>
USE db_name;

`EXAMPLE :`
```
USE hrmanagement;
```

#### **DROP DATABASE :**
>**SYNTAX :** <br> DROP DATABASE db_name;

`EXAMPLE :`
```
DROP DATABASE hrmanagement;
```

#### **CREATE TABLE :**
 
**DEFINITION :** *A table is used to organize data in the form of rows and columns and used for both storing and displaying records in the structure format. It is similar to worksheets in the spreadsheet application. A table creation command requires  **three things**:*

-   Name of the table
-   Names of fields
-   Definitions for each field 

>**SYNTAX :** <br>
CREATE TABLE `table_name`( column_definition1,<br>
  column_definition2,<br>
  ........ ,<br>
 table_constraints <br>
  );

`EXAMPLE :`
```
CREATE TABLE `employee_details` (
  `employee_id` varchar(10) NOT NULL,
  `first_name` varchar(30) NOT NULL,
  `last_name` varchar(30) DEFAULT NULL,
  `gender` varchar(10) NOT NULL,
  `date_of_birth` date NOT NULL,
  `date_joined` date NOT NULL,
  `email` varchar(255) NOT NULL,
  `contact_number` bigint NOT NULL,
  `account_number` bigint NOT NULL,
  `department_id` varchar(10) NOT NULL,
  `address_id` varchar(10) NOT NULL,
  PRIMARY KEY (`employee_id`),
  KEY `department_id` (`department_id`),
  KEY `address_id` (`address_id`),
  KEY `name_gender_id` (`first_name`,`gender`),
  CONSTRAINT `employee_details_ibfk_1` FOREIGN KEY (`department_id`) REFERENCES `department` (`department_id`),
  CONSTRAINT `employee_details_ibfk_2` FOREIGN KEY (`address_id`) REFERENCES `address` (`address_id`)
);
```
#### **ALTER :**

**DEFINITION :** *MySQL ALTER statement is used when you want to change the name of your table or any table field. It is also used to add or delete an existing column in a table.*

_NOTE :_ The ALTER statement is always used with "ADD", "DROP" and "MODIFY" commands according to the situation.

`ADD :` Add a column in a table.

>**SYNTAX :**<br>
ALTER TABLE `table_name` ADD `Column_name`(Column_definition) [ FIRST | AFTER Column_name ];

`EXAMPLE :`
```
ALTER table employee_details
ADD address_id varchar(10) not null;
```
`MODIFY :`
The MODIFY command is used to change the column definition of the table.

>**SYNTAX : **<br>
 ALTER  TABLE table_name MODIFY column_name column_definition

`EXAMPLE :`
```
ALTER table employee_details 
MODIFY column address_id varchar(10) not null unique, 
ADD constraint fk_address_id foreign key(address_id) references address(id);
```
`DROP :` 
Drop a column in table

>**SYNTAX :**<BR>
 ALTER  TABLE table_name <br>
 DROP  COLUMN column_name;

`EXAMPLE :`
 ```
 ALTER  TABLE `employee_details` 
 DROP  COLUMN `date_joined`;
```

`RENAME :` Rename a column in table

>**SYNTAX :**<br>
ALTER  TABLE table_name<br>
 CHANGE COLUMN old_name new_name
 column_definition
 
(or)

>**SYNTAX :**<br>
ALTER TABLE table_name <br>
RENAME COLUMN old_column_name <br>
TO new_column_name;

#### **TRUNCATE :**
**DEFINITION :** *The TRUNCATE statement in MySQL removes the complete data without removing its structure. It is a part of . Generally, we use this command when we want to delete an entire data from a table without removing the table structure.*

>**SYNTAX :**<BR>
TRUNCATE TABLE table_name;

`EXAMPLE :`
```
TRUNCATE TABLE department;
``` 
_NOTE :_ If we perform the TRUNCATE operation for the table that uses a foreign key constraint, we will get the following error:

```
ERROR 1217 (23000): Cannot delete  or  update a parent row: a foreign  key  constraint fails
```

In that case, we need to log into the  [MySQL] server and  **disable foreign key**  checks before executing the TRUNCATE statement as below:

```
 SET FOREIGN_KEY_CHECKS=0;
```
Now, we are able to truncate tables. After execution,  **re-enable foreign key**  checks as given below:

```
 SET FOREIGN_KEY_CHECKS=1;
```
---
## DML

**DEFINITION :** *DML(Data Manipulation Language):
 The SQL commands that deals with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.*

`COMMANDS:`<br>
> - Insert 
> - Update
> - Delete

#### **INSERT :**

**DEFINITION :** *MySQL INSERT statement is used to store or add data in MySQL table within the database. We can perform insertion of records in two ways using a single query in MySQL:*

- Insert record in a single row
- Insert record in multiple rows

>**SYNTAX :** <br>
INSERT  INTO table_name ( field1, field2,...fieldN )<br>
VALUES ( value1, value2,...valueN );

`EXAMPLE :`
```
INSERT INTO `employee_details` 
VALUES ('HLXI001','Feroz','Khan','Male','2000-11-05','2021-07-15','ferozkhan.abdul@halleyx.com',6383157595,6521478952145895,'D2','AHLXI001')
```
_TIP :_ If we want to insert **multiple records** within a single command, use the following statement:

`EXAMPLE :`
```
INSERT INTO `employee_details` 
VALUES ('HLXI001','Feroz','Khan','Male','2000-11-05','2021-07-15','ferozkhan.abdul@halleyx.com',6383157595,6521478952145895,'D2','AHLXI001'),
       ('HLXI002','Pooja','Dhandapani','Female','2001-02-18','2021-07-15','pooja.dhandapani@halleyx.com',6369675794,6523652145878969,'D2','AHLXI002'),
       ('HLXI003','Mathan','Chitrarasan','Male','2000-05-29','2021-07-15','mathanraj.chitrarasan@halleyx.com',8825888985,7952365248514569,'D3','AHLXI003');
```

#### **UPDATE :**

**DEFINITION :** *MySQL UPDATE query is a DML statement used to modify the data of the MySQL table within the database. In a real-life scenario, records are changed over a period of time. So, we need to make changes in the values of the tables also. To do so, it is required to use the UPDATE query.*

*The UPDATE statement is used with the  **SET**  and  **WHERE** . The SET clause is used to change the values of the specified column. We can update single or multiple columns at a time.*

>**Syntax:**<br>
  UPDATE table_name   <br>
  SET column_name1 = new-value1, column_name2=new-value2, ... <br>
  [WHERE Clause]



_NOTE :_

-   This statement can update values in a single table at a time.
-   We can update single or multiple columns altogether with this statement.
-   Any condition can be specified by using the WHERE clause.
-   WHERE clause is very important because sometimes we want to update only a single row, and if we omit this clause, it accidentally updates all rows of the table.

The UPDATE command supports these modifiers in MySQL:

**LOW_PRIORITY:**  This modifier instructs the statement to delay the UPDATE command's execution until no other clients reading from the table. It takes effects only for the storage engines that use only table-level locking.

**IGNORE:**  This modifier allows the statement to do not abort the execution even if errors occurred. If it finds  **duplicate-key**  conflicts, the rows are not updated.

### MySQL DELETE Statement

MySQL DELETE statement is used to remove records from the MySQL table that is no longer required in the database.  **This query in MySQL deletes a full row from the table and produces the count of deleted rows**. It also allows us to delete more than one record from the table within a single query, which is beneficial while removing large numbers of records from a table. By using the delete statement, we can also remove data based on conditions.

**Once we delete the records using this query, we cannot recover it**. Therefore before deleting any records from the table, it is recommended to  **create a backup of your database**. The database backups allow us to restore the data whenever we need it in the future.

#### **DELETE :**
>**Syntax:**<br>
> DELETE  FROM table_name WHERE condition;

`EXAMPLE :`
```
DELETE FROM employee WHERE employee_id="HLXI003";
```
---
## DQL

#### **SELECT :**

**DEFINITION :** *The SELECT statement in MySQL is used to  **fetch data from one or more tables**. We can retrieve records of all fields or specified fields that match specified criteria using this statement. It can also work with various scripting languages such as  PHP,Ruby and many more.*
>**Syntax:**<br>
 SELECT field_name1, field_name 2,... field_nameN <br>
 FROM table_name1, table_name2... <br>
 [WHERE condition] <br>
 [GROUP  BY field_name(s)] <br>
 [HAVING condition] <br>
[ORDER  BY field_name(s)] <br>
[OFFSET M ][LIMIT N];

>**Syntax for all fields:**<br>
 SELECT * FROM tables <br>
 [WHERE conditions] <br>
[GROUP  BY fieldName(s)] <br>
[HAVING condition] <br>
[ORDER  BY fieldName(s)] <br>
 [OFFSET M ][LIMIT N];

`EXAMPLE 1:`
```
SELECT * FROM employee;
```
`EXAMPLE 2:`
```
SELECT employee_id,first_name,last_name,gender FROM employee WHERE employee_id="HLXI002";
```
---
## DCL
**DEFINITION :** *DCL is short name of Data Control Language which includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.*

`COMMANDS:`<br>
> - GRANT - allow users access privileges to the database
> - REVOKE - withdraw users access privileges given by using the GRANT command

#### **GRANT :**
>**SYNTAX :**<br>
GRANT privileges<br> ON object <br>TO user;

_NOTE :_ List of Privileges that can be granted are listed below. 
- ALL PRIVILEGES
- SELECT 
- INSERT
- DELETE
- UPDATE

`EXAMPLE :`
```
GRANT all privileges 
ON `table_name`
TO `user_name`@`localhost` 
```

#### **REVOKE :**
>**SYNTAX :**<br>
REVOKE privileges <br> ON object <br>FROM user;

`EXAMPLE :`
```
REVOKE select 
ON `table_name`
TO `user_name`@`localhost`
```
---
## INDEX
**DEFINITION :** *Indexes are used to retrieve data from the database more quickly than otherwise. The users cannot see the indexes, they are just used to speed up searches/queries.*

`COMMANDS:`<br>
>CREATE INDEX - The CREATE INDEX statement is used to create indexes in tables.

>DROP INDEX - The DROP INDEX statement is used to delete an index in a table.

#### **CREATE INDEX :**
>**SYNTAX :**<br>
CREATE INDEX index_name<br>
ON table_name (column1, column2, ...);

_NOTE:_ Updating a table with indexes takes more time than updating a table without (because the indexes also need an update). So, only create indexes on columns that will be frequently searched against.

`EXAMPLE :`
```
CREATE INDEX IX_1
ON department (name);
```
#### **DROP INDEX :**
>**SYNTAX :**<br>
ALTER TABLE table_name <br>
DROP INDEX index_name;


`EXAMPLE :`
```
ALTER TABLE department
DROP INDEX IX_1;
```
---
## CLAUSES

#### **WHERE CLAUSE :**

**DEFINITION :** 
*The WHERE clause is used to filter records. It is used to extract only those records that fulfill a specified condition.*

`SYNTAX :`
>SELECT column1, column2, ...</br>
FROM table_name</br>
WHERE condition;**


`EXAMPLE :`  
```
SELECT * FROM employee_details</br>
WHERE employee_id = 'HLXI001';
```

#### **FROM CLAUSE :**

**DEFINITION :** *The MySQL FROM Clause is used to select some records from a table. It can also be used to retrieve records from multiple tables using JOIN condition.*

`SYNTAX  :` 
> SELECT column1, column2, ...
FROM table_name</br>
WHERE condition;

`EXAMPLE  :`  
```
SELECT employee_id FROM employee_details;
```


#### **ORDER BY CLAUSE :**

**DEFINITION :** *The ORDER BY keyword is used to sort the result-set in ascending or descending order. The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.*

`SYNTAX  :`
> SELECT column1, column2, ... <br>
FROM table_name</br>
ORDER BY column1, column2, ... ASC|DESC;

`EXAMPLE  :`  

    SELECT employee_id
    FROM employee_details</br> 
    ORDER BY employee_id asc;


#### **GROUP BY CLAUSE :**

**DEFINITION :** *The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country". The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.*

`SYNTAX  :` 

> SELECT column_name(s)
FROM table_name</br>
WHERE condition</br>
GROUP BY column_name(s)</br>
ORDER BY column_name(s);

`EXAMPLE  :`  

    SELECT net_salary(s)
    FROM payroll</br>
    WHERE net_salary > 20000</br>
    GROUP BY employee_id</br>
    ORDER BY employee_id asc;

---

## CONDITIONS

**AND, OR and NOT Operators**


**DEFINITION :`** *The WHERE clause can be combined with AND, OR, and NOT operators.*


The AND and OR operators are used to filter records based on more than one condition:


- The AND operator displays a record if all the conditions separated by AND are TRUE.
- The OR operator displays a record if any of the conditions separated by OR is TRUE.
- The NOT operator displays a record if the condition(s) is NOT TRUE.


    
#### **AND :**

`SYNTAX  :` 
>SELECT column1, column2, ...
FROM table_name</br>
WHERE condition1 AND condition2 AND condition3 ...;

`EXAMPLE  :`  

    SELECT * FROM employee_details
    WHERE employee_id='HLXI001' AND city='Coimbatore';

#### **OR :**

`SYNTAX  :` 
>SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;

`EXAMPLE  :`  

    SELECT * FROM employee_details
    WHERE city='Coimbatore' OR city='Tirupur';

#### **NOT :**

`SYNTAX  :` 
>SELECT column1, column2, ... <br>
FROM table_name <br>
WHERE NOT condition;

`EXAMPLE  :`  

    SELECT * FROM employee_details
    WHERE NOT city='Coimbatore';

#### **LIKE OPERATOR :**

**DEFINITION :** *The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.* <BR>
There are two wildcards often used in conjunction with the LIKE operator:

- The percent sign (%) represents zero, one, or multiple characters
- The underscore sign (_) represents one, single character

`SYNTAX  :` 
> SELECT column1, column2, ...
FROM table_name<br>
WHERE columnN LIKE pattern;

`EXAMPLE  :`  

    SELECT first_name, last_name FROM employee_details
    WHERE employee_id LIKE 'HLXI%';

#### **BETWEEN OPERATOR :**

**DEFINITION :** *The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.*

The BETWEEN operator is inclusive: begin and end values are included.

`SYNTAX  :` 
> SELECT column_name(s)
FROM table_name<br>
WHERE column_name BETWEEN value1 AND value2;

`EXAMPLE  :`  

    SELECT * FROM payroll
    WHERE net_salary BETWEEN 15000 AND 20000;

#### **IN OPERATOR :**

**DEFINITION :** *The IN operator allows you to specify multiple values in a WHERE clause.*

The IN operator is a shorthand for multiple OR conditions.


`SYNTAX  :` 
> SELECT column_name(s)
FROM table_name <BR>
WHERE column_name IN (value1, value2, ...);

`EXAMPLE  :`  

    SELECT * FROM employee_details
    WHERE city IN ('coimbatore', 'Tirupur');


**EXISTS OPERATOR**

**DEFINITION :** *The EXISTS operator is used to test for the existence of any record in a subquery.*


The EXISTS operator returns TRUE if the subquery returns one or more records.


`SYNTAX  :` 
> SELECT column_name(s)
FROM table_name<BR>
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);


`EXAMPLE  :`  

    SELECT first_name
    FROM employee_details
    WHERE EXISTS (SELECT employee_id FROM payroll 
    WHERE employee_details.employee_id =  payroll.employee_id  AND gross_salary < 20000); 
---
## Joins

**Definition :** *A SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:*

- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN

>**Syntax :** <br>
**Inner join:** <BR>
SELECT table1.column1,table1.column2,table2.column1,....<BR>
FROM table1 <BR>
INNER JOIN table2<BR>
ON table1.matching_column = table2.matching_column;<br><br>
**Left join:** <BR>
SELECT table1.column1,table1.column2,table2.column1,....<BR>
FROM table1 <BR>
LEFT JOIN table2 <BR>
ON table1.matching_column = table2.matching_column; <br><BR>
**Right  join:**<BR>
SELECT table1.column1,table1.column2,table2.column1,....<BR>
FROM table1 <BR>
Right JOIN table2<BR>
ON table1.matching_column = table2.matching_column;<br><br>
**Full join:**<BR>
SELECT table1.column1,table1.column2,table2.column1,....<BR>
FROM table1 <BR>
JOIN table2<BR>
ON table1.matching_column = table2.matching_column;

Table:
https://media.geeksforgeeks.org/wp-content/cdn-uploads/table1-3.png <br><br>


**Examples :**
```
Inner join:
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

Left join:
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
LEFT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

Right join:
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
RIGHT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

Full join:
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
FULL JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

```
---
## Aliases:
**Definition:** *Aliases are the temporary names given to table or column for the purpose of a particular SQL query. It is used when name of column or table is used other than their original names, but the modified name is only temporary.*

- Aliases are created to make table or column names more readable.
- The renaming is just a temporary change and table name does not change in the original database.
- Aliases are useful when table or column names are big or not very readable.
- These are preferred when there are more than one table involved in a query.

>**Syntax:**<br> 
**For column alias:**<br>
SELECT column as alias_name <BR>
FROM table_name; <BR>
column: fields in the table <BR>
alias_name: temporary alias name to be used in replacement of original column name <BR>
table_name: name of table <br><br>
**For table alias:**<br>
SELECT column <BR>
FROM table_name as alias_name;<BR>
column: fields in the table <BR>
table_name: name of table<BR>
alias_name: temporary alias name to be used in replacement of original tab

**Example:**
```
CREATE 
    ALGORITHM = UNDEFINED 
    DEFINER = `root`@`localhost` 
    SQL SECURITY DEFINER
VIEW `realparsmodel`.`demoviews` AS
    SELECT 
        `e`.`firstName` AS `firstName`,
        `o`.`orderNumber` AS `orderNumber`,
        `o`.`courseCode` AS `courseCode`
    FROM
        (`realparsmodel`.`employees` `e`
        JOIN `realparsmodel`.`orderdetails` `o`)
    WHERE
        (`o`.`priceEach` > 170)
```
---
## Aggregate functions:

**Definition:** *An aggregate function performs a calculation on a set of values, and returns a single value. Except for COUNT( * ), aggregate functions ignore null values. Aggregate functions are often used with the GROUP BY clause of the SELECT statement.*

- Count()
- Sum()
- Avg()
- Min()
- Max()

>**Synatx:** <br>
COUNT(*)  
or  
COUNT( [ALL|DISTINCT] expression )  <br><br>
SUM()  
or  
SUM( [ALL|DISTINCT] expression )  <br><br>
AVG()  
or  
AVG( [ALL|DISTINCT] expression )  <br><br>
MAX()  
or  
MAX( [ALL|DISTINCT] expression )  <br><br>
MIN()  
or  
MIN( [ALL|DISTINCT] expression )  

**Examples:** 
```
SELECT COUNT(*)  
FROM PRODUCT_MAST;  

SELECT SUM(COST)  
FROM PRODUCT_MAST  
WHERE QTY>3;  

SELECT AVG(COST)  
FROM PRODUCT_MAST;  

SELECT MAX(RATE)  
FROM PRODUCT_MAST;  

SELECT MIN(RATE)  
FROM PRODUCT_MAST;  
```
---