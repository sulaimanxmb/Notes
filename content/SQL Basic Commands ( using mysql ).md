### Database Related Commands :
- #### To create a database :
	```mySQL 
CREATE DATABASE   database_name  ;
	 ```
There is a default database already present called sys

- #### To use your database :
```mySQL
USE  database_name  ;
```

- #### To Delete your Database
```mySQL
DROP DATABASE  database name  ;
```

- #### To make your database in readonly mode :
```mySQL
ALTER DATABASE  database_name  `READ ONLY = 1`;
```

### Table related commands :
- #### To create a Table :
	```mySQL
CREATE TABLE table_name  ( Column1 INT, Column2 VARCHAR(50), Column3 DECIMAL(5,2), Column4 DATE ) ;
```

	`INT` - this data type is used for only numbers/integers
	`VARCHAR (MAX DIGITS)` - this data type is used for only alphabetical characters
	`DECIMAL(MAX DIGIT, PRESISION)` - this data type is used only for decimal integers
	`DATE` - this data type is used only for entering date

- #### To Select / Show Table :
	```mySQL
SELECT * FROM  table_name ;
```

- #### To Rename a table :
	```mySQL
RENAME TABLE old_name TO new_name ;
```

- #### To delete a table :
```mySQL
DROP TABLE table_name ;
```

### Column Related Commands :

- #### To add  a column to the table :
	```mySQl
ALTER TABLE table_name ADD new_table_name VARCHAR(15) ;
```
	

- #### To rename a column :
```mySQL
ALTER TABEL table_name  RENAME COLUMN old_column TO new_column ;
```

- #### To change a column data type :
```mySQL
ALTER TABLE  table_name  MODIFY COLUMN column_name  VARCHAR(20) ;
```

- #### To change the position of a column :
	```mySQL
ALTER TABLE  table_name  MODIFY  column_name  VARCHAR(100)  AFTER after_which_column_it_should_come ;
```

- #### To change position of column to first :
```mySQl
ALTER TABLE  table_name  MODIFY  coulmn_name  VARCHAR(100) FIRST ;
```

- #### To delete a column :
```mySQL
ALTER TABLE  table_name DROP COLUMN column_name  ;
```
	

### Row Related Commands :

- #### To create a single row :
	```mySQL
INSERT INTO table_name VALUES ( 1, “ Name ”, 23.56, “ 2024-12-25 “) ;
```
	
	For `INT` data type Ex : 1
	
	For `VARCHAR` data type Ex : “ Name “
	
	For `DATE` data type Ex : “ YYYY-MM-DD “

- #### To create multiple rows at same time :
	```mySQL
INSERT INTO table_name VALUES    ( 2, “Name1" , 21.10, “ 2023-11-1“) 
	                             ( 3, “Name2 “, 20.99, “ 2022-12-31“) 
	                             (  ……….etc………….) ;
```
                                    
- #### To delete a row :
	`DELETE FROM` table_name `WHERE` coulmn_name = 6 ;

### Data Commands :

- #### To show only particular column :
```mySQL
SELECT column_name1, column_name2 FROM table_name
```

- #### To search a Particular Data :
```mySQL
SELECT * FROM table_name WHERE column_name = 3 ( given data type is INT ) ;
```
Also works with  :
```mySQl
WHERE column_name >= 12 ( data type is INT so ) ;
```
Also works with  : 
```mysql
WHERE column_name != “Name1“ ( Not equal to) ;
```
