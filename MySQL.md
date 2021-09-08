# MySQL

# Table of Contents
- [Entity Relationship Diagram](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#entity-relationship-diagram-erd)
- [Data Definition Language (DDL)](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#data-definition-language-ddl)
	- [Create Database](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#create-database-)
	- [Drop Database](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#drop-database-)
	- [Create Table](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#create-table-)
	- [Alter](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#alter-)
	- [Truncate](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#truncate-)
- [Data Manipulation Language (DML)](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#data-manipulation-language-dml)
	- [Insert](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#insert-)
	- [Update](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#update-)
	- [Delete](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#mysql-delete-statement)
- [Data Query Language (DQL)](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#data-query-language-dql)
	- [Select](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#select-)
- [Data Control Language (DCL)](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#data-control-language-dcl)
	- [Grant](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#grant-)
	- [Revoke](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#revoke-)
- [Index](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#index)
	- [Create Index](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#create-index-)
	-  [Drop Index](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#drop-index-)
- [Clauses](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#clauses)
	- [Where Clause](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#where-clause-)
	- [From Clause](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#from-clause-)
	- [Order By Clause](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#order-by-clause-)
	- [Group By Clause](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#group-by-clause-)
- [Conditions](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#conditions)
	- [And Operator](3eb46242aad791aefa762d89a01f631aa5c09f1c73c3bae55df33bcaaa769c33caeea5adbc48)
	- [Or Operator](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#or-)
	- [Not Operator](3eb46242aad791aefa762d89a01f631aa5c09f1c73c3bae55df33bcaaa769c33caeea5adbc48)
	- [Like Operator](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#like-operator-)
	- [Between Operator](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#between-operator-)
	- [In Operator](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#in-operator-)
- [Joins](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#joins)
- [Aliases](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#aliases)
- [Aggregate functions](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#aggregate-functions)
- [Stored Procedure Basics](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#stored-procedure-basics)
	- [Executing A Stored Procedure](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#executing-a-stored-procedure-)
        - [In Parameters](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#in-parameters-)
        - [Out Parameters](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#out--parameters-)
        - [InOut Parameters](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#inout--parameters-)
- [Temporary Table](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#mysql-temporary-table)
	- [Temporary Table](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#mysql-temporary-table)
	- [Create Temporary Table](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#mysql--create-temporary-table--statement)
- [Views](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#mysql-views)
- [Functions](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#functions)
- [Trigger](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#trigger)
- [Cursor](https://github.com/ganesh-design/Documentation/blob/main/MySQL%20(1).md#cursor)


## **Entity Relationship Diagram (ERD)**
**Definition :** *It is a technique to document a software system using diagrams and symbols. It is used to represent communication of data.*

*The highest level of abstraction for the data model is called the Entity Relationship Diagram (ERD). It is a graphical representation of data requirements for a database.*

*There are three components in ERD.*

- **Entities:** Number of tables you need for your database. <br>
- **Attributes:** Information such as property, facts you need to describe each table. <br>
- **Relationships:** How tables are linked together. These relationships are denoted by crow's foot symbols.<br>

**Entity :**
Entities are the basic objects of ERDs. These are the tables of your database.

**Relationships :**
Relationships are the associations between the entities. Verbs often describe relationships between entities. We will use Crow's Foot Symbols to represent the relationships.

**Example :**
<img src="https://www.cs.uregina.ca/Links/class-info/215/images/relationship.png"/>

**`One to One Relationship (1:1) :`**
A single entity instance in one entity class is related to a single entity instance in another entity class.

**`For example:`**
- Each student fills one seat and one seat is assigned to only one student.

**`One to Many Relationship (1:M) :`**
A single entity instance in one entity class (parent) is related to multiple entity instances in another entity class (child)

**`For example:`**
- One instructor can teach many courses, but one course can only be taught by one instructor.

**`Many to Many Relationship (M:M) :`**
Each entity instance in one entity class is related to multiple entity instances in another entity class; and vice versa.

**`For example:`**
- Each student can take many classes, and each class can be taken by many students.

**Attributes :**
Attributes are facts or description of entities. They are also often nouns and become the columns of the table. For example, for entity student, the attributes can be first name, last name, email, address and phone numbers.
- **Primary Key :**
Primary Key* or identifier is an attribute or a set of attributes that uniquely identifies an instance of the entity. 
- **Foreign key :**
A foreign key+ (sometimes called a referencing key) is a key used to link two tables together. Typically you take the primary key field from one table and insert it into the other table where it becomes a foreign key

---
## **Data Definition Language (DDL)**

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
## Data Manipulation Language (DML)

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
## **Data Query Language (DQL)**

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
## **Data Control Language (DCL)**
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
## **INDEX**
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
## **CLAUSES**

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

## **CONDITIONS**

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
## **Joins**

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
<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/table1-3.png "/>

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
## **Aliases:**
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
## **Aggregate functions:**

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
## **STORED PROCEDURE BASICS**
**DEFINITION :**
*When you use MySQL Workbench or mysql shell to issue the query to MySQL Server, MySQL processes the query and returns the result set.*

If you want to save this query on the database server for execution later, one way to do it is to use a stored [procedure](https://www.mysqltutorial.org/mysql-stored-procedure-tutorial.aspx).

The following  [CREATE PROCEDURE](https://www.mysqltutorial.org/getting-started-with-mysql-stored-procedures.aspx)  statement creates a new stored procedure 

**SYNTAX :**
>CREATE PROCEDURE procedure_name(parameter_list)<br>
BEGIN<br>
   statements;<br>
END<br>

**EXAMPLE :**
```
DELIMITER $$
CREATE DEFINER=`root`@`localhost` PROCEDURE `Salary_credit`(in employee varchar(100),in payroll_id varchar(100))
BEGIN
	drop temporary table if exists  credited_salary;
	create temporary table if not exists credited_salary
	select  pr.employee_id ,concat(e.first_name,' ',e.last_name) as name, pr.net_salary from payroll pr join employee_details e on e.employee_id = employee and payroll_id=pr.payroll_id;
END$$
DELIMITER ;
```
-   First, change the default delimiter to  `$$`.
-   Second, use (`;`) in the body of the stored procedure and  `$$`  after the  `END`  keyword to end the stored procedure.
-   Third, change the default delimiter back to a semicolon (;)

#### **EXECUTING A STORED PROCEDURE :**

To execute a stored procedure, you use the  `CALL`  statement:
\
**SYNTAX :**


>CALL stored_procedure_name(argument_list);


In this syntax, you specify the name of the stored procedure after the  `CALL`  keyword. If the stored procedure has parameters, you need to pass arguments inside parentheses following the stored procedure name.

	call the procedure with 
	`CALL Salary_credit('EMP001','PAYID001');`
	here we use `IN` parameter

#### **IN PARAMETERS :**
**DEFINITION :**
*`IN`  is the default mode. When you define an  `IN`  parameter in a stored procedure, the calling program has to pass an argument to the stored procedure.*

**EXAMPLE**
```
DELIMITER $$
CREATE DEFINER=`root`@`localhost` PROCEDURE `Salary_credit`(in employee varchar(100),in payroll_id varchar(100))
BEGIN
	drop temporary table if exists  credited_salary;
	create temporary table if not exists credited_salary
	select  pr.employee_id ,concat(e.first_name,' ',e.last_name) as name, pr.net_salary from payroll pr join employee_details e on e.employee_id = employee and payroll_id=pr.payroll_id;
END$$
DELIMITER ;
```		
#### **OUT  PARAMETERS :**
**DEFINITION :** *The value of an  `OUT`  parameter can be changed inside the stored procedure and its new value is passed back to the calling program.*

Notice that the stored procedure cannot access the initial value of the  `OUT`  parameter when it starts.
#### **INOUT  PARAMETERS :**
**DEFINITION :**
*An  `INOUT`  parameter is a combination of  `IN`  and  `OUT`  parameters. It means that the calling program may pass the argument, and the stored procedure can modify the  `INOUT`  parameter, and pass the new value back to the calling program.*

#### **Using PARAMETER [ IN | OUT | INOUT ]**
```
CREATE DEFINER=`root`@`localhost` PROCEDURE `Salary_credit`(in employee varchar(100),inout payroll_id varchar(100),out name varchar(30))
BEGIN
	drop temporary table if exists  credited_salary;
    select concat(first_name,' ',last_name)  into name from employee_details where employee_id=employee;
	create temporary table if not exists credited_salary
	select  pr.employee_id ,concat(e.first_name,' ',e.last_name) as name, pr.net_salary from payroll pr join employee_details e on e.employee_id = employee and payroll_id=pr.payroll_id;
END
```
here we use `IN` and `OUT` and `INOUT`
**Drop** the procedure using<br>
**SYNTAX :**

>DROP  PROCEDURE  IF  EXISTS invoke_hr_procedure;

The statement  `SHOW WARNINGS`  shows the warning:

`SHOW WARNINGS;`
here we call that procedure with trigger that's fired when payroll insertion occur.

**Sample :**

```
drop trigger salary_notifier;
DELIMITER //
CREATE TRIGGER `salary_notifier`
AFTER INSERT ON payroll
FOR EACH ROW
BEGIN
	call Salary_credit(new.employee_id,new.payroll_id,@name);
END//
DELIMITER ;
```
#### **MySQL TEMPORARY TABLE**
**DEFINITION :**
*In MySQL, a temporary table is a special type of table that allows you to store a temporary result set, which you can reuse several times in a single session.*

A MySQL temporary table has the following specialized features:

-   A temporary table is created by using  `CREATE TEMPORARY TABLE`  statement. Notice that the keyword  `TEMPORARY`  is added between the `CREATE`  and  `TABLE`  keywords.
-   MySQL removes the temporary table automatically when the session ends or the connection is terminated. Of course, you can use the [`DROP TABLE`](https://www.mysqltutorial.org/mysql-drop-table)  statement to remove a temporary table explicitly when you are no longer use it.
-   A temporary table is only available and accessible to the client that creates it. Different clients can create temporary tables with the same name without causing errors because only the client that creates the temporary table can see it. However, in the same session, two temporary tables cannot share the same name.
-   A temporary table can have the same name as a normal table in a database. For example, if you create a temporary table named  `employees`  in the  [sample database](https://www.mysqltutorial.org/mysql-sample-database.aspx "MySQL Sample Database"), the existing  `employees`  table becomes inaccessible. Every query you issue against the  `employees`  table is now referring to the temporary table `employees`. When you drop the  `employees`  temporary table, the permanent  `employees`  table is available and accessible.

Even though a temporary table can have the same name as a permanent table, it is not recommended. Because this may lead to confusion and potentially cause an unexpected data loss.
#### **MySQL  CREATE TEMPORARY TABLE  STATEMENT**
**SYNTAX :** 
>CREATE TEMPORARY TABLE table_name(
   column_1_definition,
   column_2_definition,
   ...,
   table_constraints
);

**EXAMPLE:**
```

CREATE DEFINER=`root`@`localhost` PROCEDURE `Salary_credit`(in employee varchar(100),inout payroll_id varchar(100),out name varchar(30))
BEGIN
	drop temporary table if exists  credited_salary;
    select concat(first_name,' ',last_name)  into name from employee_details where employee_id=employee;
	create temporary table if not exists credited_salary
	select  pr.employee_id ,concat(e.first_name,' ',e.last_name) as name, pr.net_salary from payroll pr join employee_details e on e.employee_id = employee and payroll_id=pr.payroll_id;
END
```
The syntax of the  `CREATE TEMPORARY TABLE`  staetment is similar to the syntax of the  `CREATE TABLE`  statement except for the  `TEMPORARY`  keyword.
Here we **create** temporary table called `credited_salary` with some expression .

**DROP TEMPORARY TABLE**
**SYNTAX :**

>DROP TEMPORARY TABLE IF EXISTS  temporary_table_name;

**EXAMPLE:**
```
DROP TEMPORARY TABLE IF EXISTS  credited_salary;
```
---
## **MySQL Views**
This is to save the query in the database server and assign a name to it. This named query is called a  **database view,**  or simply,  **view**.

By definition, a view is a named query stored in the database catalog.

To create a new view you use the  [CREATE VIEW](https://www.mysqltutorial.org/create-sql-views-mysql.aspx) statement. This statement creates a view

**SYNTAX :**

>CREATE  VIEW  _view_name_  AS  
SELECT  _column1_,  _column2_, ...  
FROM  _table_name_  
WHERE  _condition_;

_NOTE :_  A view always shows up-to-date data! The database engine recreates the view, every time a user queries it.

**EXAMPLE :**
```
CREATE DEFINER=`root`@`localhost` PROCEDURE `Salary_credit`(in employee varchar(100),inout payroll_id varchar(100),out name varchar(30))
BEGIN
	drop temporary table if exists  credited_salary;
    select concat(first_name,' ',last_name)  into name from employee_details where employee_id=employee;
	create temporary table if not exists credited_salary
	select  pr.employee_id ,concat(e.first_name,' ',e.last_name) as name, pr.net_salary from payroll pr join employee_details e on e.employee_id = employee and payroll_id=pr.payroll_id;
    create view  salary_view as select*from credited_salary;
END
```
here we come with same example on procedure with create view;
#### **SQL UPDATING A VIEW**

A view can be updated with the  `CREATE OR REPLACE VIEW`  statement.

**SQL CREATE OR REPLACE VIEW SYNTAX :**


>CREATE  OR  REPLACE  VIEW  _view_name_  AS  
SELECT  _column1_,  _column2_, ...  
FROM  _table_name_  
WHERE  _condition_;

**call**  view using `select*from salary_view;`
#### **SQL Dropping a View**

A view is deleted with the  `DROP VIEW`  statement.

**SQL DROP VIEW SYNTAX :**

>DROP  VIEW  _view_name_;

**Example :**
 	
	 DROP  VIEW salary_view;
 
MySQL treats the views as tables with the type  `'VIEW'`. Therefore, to show all  [views](https://www.mysqltutorial.org/mysql-views-tutorial.aspx)  in the current database, you use the  `[SHOW FULL TABLES](https://www.mysqltutorial.org/mysql-show-tables/)`  statement as follows:

`SHOW FULL TABLES 
WHERE table_type = 'VIEW';` 

Code language: SQL (Structured Query Language) (sql)

Because the  SHOW FULL TABLES`  statement returns both tables and views, you need to add a  `[WHERE](https://www.mysqltutorial.org/mysql-where/)`  clause to get the views only.

---
## **Functions**

**Definition :** *The CREATE FUNCTION statement is used for creating a stored function and user-defined functions. A stored function is a set of SQL statements that perform some operation and return a single value.*

*Just like Mysql in-built function, it can be called from within a Mysql statement.*

*By default, the stored function is associated with the default database.*

>**SYNTAX :** <br>
CREATE FUNCTION function_name(func_parameter1, func_parameter2, ..) <br>
          RETURN datatype [characteristics] <br>
          func_body

**Parameters used:**

- **function_name:**
It is the name by which stored function is called. The name should not be same as native(built_in) function. In order to associate routine explicitly with a specific database function name should be given as database_name.func_name.

- **func_parameter:**
It is the argument whose value is used by the function inside its body. You can’t specify to these parameters IN, OUT, INOUT. The parameter declaration inside parenthesis is provided as func_parameter type. Here, type represents a valid Mysql datatype.

- **datatype:**
It is datatype of value returned by function.
characteristics:
The CREATE FUNCTION statement is accepted only if at least one of the characterisitics { DETERMINISTIC, NO SQL, or READS SQL DATA } is specified in its declaration.

**func_body** is the set of Mysql statements that perform operation. It’s structure is as follows:

>**func_body :** <br>
BEGIN <br>
Mysql Statements<br>
    RETURN expression; <br>
END

_NOTE :_ The function body must contain one RETURN statement.

**Example :**
```
CREATE DEFINER=`root`@`localhost` FUNCTION `income`(gross_salary bigint, gross_deductions bigint) RETURNS bigint
    READS SQL DATA
    DETERMINISTIC
BEGIN
DECLARE income bigint;
SET income = 0;
-- label1: WHILE income <= 3000 DO
SET income = gross_salary - gross_deductions;
-- END WHILE label1;
RETURN income;
END
```

To call the above function :

    select employee.income(22000, 2000);
---
## **Trigger**


**Definition:** *The Triggers subtab opens a workspace that enables you to create new triggers or edit existing triggers. All triggers are organized within a tree structure by section, such as BEFORE INSERT and AFTER INSERT.*

To add a new trigger, click the [+] icon next to the trigger section. To delete a trigger, click the associated [-] icon. These icons become visible by hovering over a trigger or trigger section. Click Apply to commit your changes. The next figure shows an example of the customer_create_date trigger.

>**syntax:** <br>
CREATE TRIGGER trigger_name <br>
{BEFORE | AFTER} {INSERT | UPDATE| DELETE }<br>
ON table_name FOR EACH ROW <br>
trigger_body;

**Example:**
```
CREATE TABLE employees_audit (
    id INT AUTO_INCREMENT PRIMARY KEY,
    employeeNumber INT NOT NULL,
    lastname VARCHAR(50) NOT NULL,
    changedat DATETIME DEFAULT NULL,
    action VARCHAR(50) DEFAULT NULL
);
CREATE TRIGGER before_employee_update 
    BEFORE UPDATE ON employees
    FOR EACH ROW 
 INSERT INTO employees_audit
 SET action = 'update',
     employeeNumber = OLD.employeeNumber,
     lastname = OLD.lastname,
     changedat = NOW();
     SHOW TRIGGERS;
     UPDATE employees 
SET 
    lastName = 'Phan'
WHERE
    employeeNumber = 1056;
    SELECT * FROM employees_audit;
```
---
## **Cursor**

**Definition:**  *A cursor allows to iterate a set of rows returned by a query and process them accordingly. We create cursor inside a stored procedure to handle the result set returned by a query. Mysql cursors are read-only and non-scrollable.* <br><br>


 >**SYNTAX:**<br>
 Declare<cursor_name> for select_statement <br>
  Open <cursor_name> initializes the result set for operation <br>
  Fetch cursor_name into variable list to retrieve the next row pointed by the cursor and move the cursor to the next row in the result set. <br>
  Close <cursor_name>to deactivate the cursor and release any memory associated with it.


**Example:**
```
   delimiter $$
   create procedure proc_emp()
   begin
   declare v_ename varchar(100);
   declare v_salary int;
   declare v_finished integer default 0;
   declare c1 cursor for select ename ,salary from employees;
   declare continue handler for NOT FOUND set v_finished=1;
   open c1;
   get_emp:LOOP
      fetch c1 into v_ename , v_salary;
      if v_finished=1 then 
          leave get_emp;
      end if;
      select concat (v_ename,v_salary);
      END LOOP get_emp;
      close c1;
    end $$
```

---
