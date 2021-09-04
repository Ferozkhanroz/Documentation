## DCL
**DEFINITION :** *DCL is short name of Data Control Language which includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.*

`COMMANDS:`<br>
>GRANT - allow users access privileges to the database

>REVOKE - withdraw users access privileges given by using the GRANT command

### `GRANT :`
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

### `REVOKE :`
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

<u>`CREATE INDEX :`</u>
>**SYNTAX :**<br>
CREATE INDEX index_name<br>
ON table_name (column1, column2, ...);

_NOTE:_ Updating a table with indexes takes more time than updating a table without (because the indexes also need an update). So, only create indexes on columns that will be frequently searched against.

`EXAMPLE :`
```
CREATE INDEX IX_1
ON department (name);
```
<u>`DROP INDEX :`</u>
>**SYNTAX :**<br>
ALTER TABLE table_name <br>
DROP INDEX index_name;


`EXAMPLE :`
```
ALTER TABLE department
DROP INDEX IX_1;
```
---