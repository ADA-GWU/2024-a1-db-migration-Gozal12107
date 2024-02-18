[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/JwSLLxUh)
# Assignment1 

Migration is a type of process that ensures the transformation of the database structure. Throughout the process, it also preserves the data integrity. To begin the migration, a migration procedure should be executed. The following steps identify a migration process:

## Migration Process
1.	Column name _ST_ID_ in the _STUDENTS_ table will be replaced with _STUDENT_ID_ by using the `ALTER TABLE` command.
2.	The length of the columns _ST_NAME_ and _ST_LAST_ in the _STUDENTS_ table will be changed from 20 to 30 by using the `ALTER TABLE` command again.
3.	A new column of _INTERESTS_ will be created in the _INTERESTS_ table as the type ARRAY of strings by using the `ALTER TABLE` command again.
4.	Existing values in the _INTERESTS_ table will be converted into an ARRAY of strings, and these new values will be updated in the _INTERESTS_ column. This can be achieved by using a combination of commands such as  `STRING_AGG` and `ARRAY_TO_STRING`.
5.	Initially defined column _INTEREST_ in the table _INTERESTS_ will be dropped by using the `ALTER TABLE` command.
