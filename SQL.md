# SQL
This page made by student.
My personal notebook.

***

#### Table of Contents
- [Your first steps at Databases](#Your-first-steps-at-databases)
- [USE/SELECT](#Use-and-Select)
- [Types of Variables](#Types-of-Variables)
- [Tables](#Tables)
    - [Exercise Tables](#Work-on-Tables)
    
- [Warning](#Warnings)
- [Key](#Key)
- [Default](#Default-Values)
- [Where](#Where)
- [Alieses](#Alieses)
- [Update](#Update)
- [Delete](#Delete)
- [Concat](#Concat)
- [Substring](#Substring)
- [CombineComamnds](#CombineComamnds)
- [Replace](#Replace)
- [Reverse](#Reverse)
- [Char Lenght](#Char-Lenght)
- [Upper/Lower](#Upper/Lower)
- [Distinct](#Distinct)
- [ORDER_BY](#ORDER_BY)
- [Limit](#Limit)
- [Like](#Like)





***
## Your first steps at databases
1. **CREATE DATABASE** < database name >;
> - Create database with name that you choose

2. **SHOW DATABASES;**
> - Show all created databases

3. **DROP DATABASE** < database name >;
 > - Delete database that you choose
***

## Use and Select
1. **USE**  < database name >;
> - Answer to this command is : Data base changed

2. **SELECT**  < database name >;
> - What was the name of last Database that we used.
>   Last dabases that we used command USE on it.
***

## Tables
We have columns and rows. Lets see it :

|  | First_Name | Last_Name | Age  |
|--|------------|-----------|------|
|1.| Slava      | Faigen    |   30 |
|2.| Idit       | Miron     |   26 |


Rows : 1, 2.

Columns : First_Name, Last_Name, Age.



1. **CREATE TABLE** < table name >(

   < column name > < data type >
 
   );
   
> **CREATE TABLE** family (
> First_Name VARCHAR(50),

> Last_Name VARCHAR(50),

> Age INT 

> );

2. **SHOW TABLES**;
> - Show tables at your database

3. **SHOW COLUMNS FROM** < table name >;
> - Show columns from your table

4. **DESC** < table name >;
> - Describe your table. Will show you table columns and types of variables in it.

5. **DROP TABLE** < table name>;
> - Delete your table

6. **INSERT INTO** < table name > ( < column_name1 > , < column_name2 > )

   **VALUES** ( < value1 > , < value2 > );
> - Fill your table.   
> **INSERT INTO** family (First_name ,Last_name, Age)
>
>   **VALUES** ('Slava','Faigen',30), 
>
>   ('Idit','Miron',26);

7. **SELECT * FROM** < table name> ;
> - Show your table content

8. **SELECT** < column_name > **FROM** < table_name>;
> - Show spesific column from your table.

***

## Types of Variables
1. **INT** 
> - Integer . Examples : 5, 100 , 0 , -63...
> - Size : -2^31 (-2,147,483,648) to 2^31-1 (2,147,483,647)

2. **VARCHAR(N)**
> - Text variable
> - N is amount of chars(size of varchar, lenght of the word)
> - VARCHAR(3): word built form 3 chars (cat, dog, egg, koi, BMW, six)

***

## Warnings

1. **SHOW WARNINGS**;
> - Show all wanings. If you use other command after you got warnings, you will not see the warnings.
***

## How to work with NULL?

Null is not **ZERO**!
Value unknown!

***

## Work on Tables

Create table for 3 of my pets.
I have 2 cats and a dog.
- Female cat named : Cholera . She is 3 years old.
- Male cat named :Perach. He is 3 years old.
- Female dog : Pie. She is 2 years old.
Good luck!

[Solution](#Solution-Tables)


       
***
## Default Values

If you forgot or you dont want to fill table with data , SQL will do it for you and put the default value there.

CREATE TABLE workers(

name VARCHAR(100) DEFAULT 'No name provided',

age INT DEFAULT 00);


*Also you can prohibit using NULL value:*

CREATE TABLE workers(

name VARCHAR(100) NOT NULL DEFAULT 'No name provided',

age INT NOT NULL DEFAULT 00);
***

## Key
Unique identifier. To identify between different "worker" but with the same name we give them primary key.
Evryone has his own primery key. We can enter it or we can ask from SQL to do this.

CREATE TABLE workers(worker_id INT NOT NULL,
name VARCHAR(100),
PRIMERY KEY(worker_id));

*SQL automatic fill the Key:*

CREATE TABLE workers(worker_id INT NOT NULL AUTO_INCREMENT,
name VARCHAR(100),
PRIMERY KEY(worker_id));

***

## Where

1. **SELECT** * **FROM** < table_name > **WHERE** < column_name > = ' < VARCHAR()> '; 
> When column variables are VARCHAR()


2. **SELECT** * **FROM** < table_name > **WHERE** < column_name > = < number >;
> When column variables are INT

***

## Alieses

Take your column name and call it with other name .

**SELECT** < column_name > **AS** <new_column_name> ;
***

## Update

How do we alter the existing data?  **THERE IS NO UNDO BUTTON !!!**

1. **UPDATE** < table_name > **SET** < colunm_name >='< VARCHAR() >' 

   **WHERE** < column_name >='<VARCHAR() >';

2. **UPDATE** < table_name > **SET** < colunm_name >= < number > 

   **WHERE** < column_name >='<VARCHAR() >';

3. **UPDATE** < table_name > **SET** < colunm_name >='< VARCHAR() >' 

   **WHERE** < column_name >=< number >;

***

## Delete

How to delete !

**DELETE** < table_name > **WHERE** <column_name>='< VARCHAR() >' ;

> - For VARCHAR()

**DELETE** < table_name > **WHERE** <column_name>= < number > ;

> - For INTeger


***

## Concat

Combine columns to new table. 

**SELECT CONCAT** (< columns_name> , < column_name >)
**FROM** < table_name >;

> - There is no separator bettwen new columns

**SELECT CONCAT_WS** (< The Separator > , < column_name2 > , < column_name2 >)
**FROM** < table_name >;

> - With Separator

***

## Substring

1. **SELECT SUBSTRING** ('Hello World!',1,4);

> - Output: Hell

2. **SELECT SUBSTRING** ('Hello World!', 7);

> - Output: Hello W

3. **SELECT SUBSTRING** ("Hello! I'm a student", 1 , 14 )

> - Output: Hello! I'm a s

4. **SELECT SUBSTRING** (< column_name >, < first_char >, < last_char >)
   **FROM** <table_name>;

***   

## Replace

Replace parts of strings.

1. **SELECT REPLACE** ('Hello World', 'Hell', '1234');

> - Output: 1234o World

2. **SELECT REPLACE** (< column_name >, '< char you want to replace >' , '< new char that you replace with >' )

   **FROM** <table_name> ;
  
***

## Reverse

Super straight forward!

1. **SELECT REVERSE** ('Hello World')

> - Output: dlroW olleH

2. **SELECT REVERSE** (<column_name>)

   **FROM** <table_name>;
   
***

## Char Lenght

Counts characters in string

1. **SELECT CHAR_LENGHT** ('Hello World');

> - Output: 11

2. **SELECT**  <column_name>, **CHAR_LENGHT** (<column_name>)
   **FROM** <table_name>;

***

## Upper/Lower

Change a string's case

**SELECT UPPER** ('Hello world');

> - Output: HELLO WORLD

**SELECT LOWER** ('HELLO WORLD');

> - Output: hello world

 **SELECT UPPER/LOWER** (<column_name>)
   **FROM** <table_name>;

***

## CombineComamnds

**SELECT**

        **CONCAT**(
                   **SUBSTRING** (< column_name >, 1 , 13), '...'
                   )                
                   **AS** 'new_column_name'
                    **FROM** < table_name >;
              

***

## Solution Tables

CREATE DATABASE pet;

USE pet;

CREATE TABLE pets(

Breed VARCHAR(3),

Sex VARCHAR(6),

Name VARCHAR(100),

Age INT

);

INSERT INTO pets(Breed, Sex, Name, Age)

VALUES ('cat', 'female', 'Cholera' , 3), ('cat', 'male', 'Perach', 3), ('dog', 'female', 'Pie', 2);
