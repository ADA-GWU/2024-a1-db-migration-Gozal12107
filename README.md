[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/JwSLLxUh)
# Assignment1 

Migration is a type of process that ensures the transformation of the database structure. Throughout the process, it also preserves the data integrity. To begin the migration, a migration procedure should be executed. The following steps identify a migration process:

## Migration Process
1.	Column name _ST_ID_ in the _STUDENTS_ table will be replaced with _STUDENT_ID_ by using the `ALTER TABLE` command.
2.	The length of the columns _ST_NAME_ and _ST_LAST_ in the _STUDENTS_ table will be changed from 20 to 30 by using the `ALTER TABLE` command again.
3.	A new column of _INTERESTS_ will be created in the _INTERESTS_ table as the type ARRAY of strings by using the `ALTER TABLE` command again.
4.	Existing values in the _INTERESTS_ table will be converted into an ARRAY of strings, and these new values will be updated in the _INTERESTS_ column. This can be achieved by using a combination of commands such as  `STRING_AGG` and `ARRAY_TO_STRING`.
5.	Initially defined column _INTEREST_ in the table _INTERESTS_ will be dropped by using the `ALTER TABLE` command.

The implication of this procedure will modify the ‘STUDENTS’ and ‘INTERESTS’ tables according to the given requirements. Verification of the changes in the database can be checked by the queries applied to the tables (e.g.: SELECT * FROM STUDENTS). 
If the need to revert the changes during the migration appears, the rollback procedure should be executed to restore the initial structure of the database.  The following steps identify a rollback process:

## Rollback Process
1.	A new column of _INTEREST_ will be created in the _INTERESTS_ table as the type **STRING(20)**.
2.	The “INTEREST” column in the _INTERESTS_ table will be filled with the values in the _INTERESTS_ column by using the `unnest` function. The `unnest` function takes an **ARRAY** and returns each element contained in this **ARRAY** as a single row in the table (Here in the _INTERESTS_ table).
3.	The column _INTERESTS_ in the table _INTERESTS_ will be dropped.
4.	The length of the columns _ST_NAME_ and _ST_LAST_ in the _STUDENTS_ table will be changed back to 20 from 30.
5.	Column name _STUDENT_ID_ in the _STUDENTS_ table will be renamed back to _ST_ID_.

Verification of the changes in the database after the rollback procedure can be checked by the queries applied to the tables 
(e.g.: `SELECT * FROM STUDENTS`).

### Note:
 **It is recommended to do testing after each procedure, respectively. Before applying procedures, essential backups should be considered to prevent any potential risks.**






