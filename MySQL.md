## DCL
**DEFINITION :** *DCL is short name of Data Control Language which includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.*

`COMMANDS:`<br>
>GRANT - allow users access privileges to the database <br>
REVOKE - withdraw users access privileges given by using the GRANT command

`SYNTAX :`
>GRANT privileges<br> ON object <br>TO user;

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
