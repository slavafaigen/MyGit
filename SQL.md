# SQL
explanation about what this page is !
***

#### Table of Contents
- [Your first steps at Databases](#Your-first-steps-at-databases)
- [USE/SELECT](#Use-and-Select)
- [Types of Variables](#Types-of-Variables)
- [Tables](#Tables)


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
|2.| Idit       | Faigen    |   26 |
Rows : 1, 2.
Columns : First_Name, Last_Name, Age.



1. **CREATE TABLE** < table name >(

 < column name > < data type >
 
  );
  
> **CREATE TABLE** family(
> First_Name VARCHAR(50),

> Last_Name VARCHAR(50),

> Age INT 

> );

2. **SHOW TABLES**;
> - Show tables at your database

3.**SHOW COLUMNS FROM** < table name >;
> - Show columns from your table

4. **DESC** < table name >;
> - Describe your table. Will show you table columns and types of variables in it.


***

## Types of Variables
1. **INT** 
> - Integer . Examples : 5, 100 , 0 , -63...
> - Size : -2^31 (-2,147,483,648) to 2^31-1 (2,147,483,647)

2. **VARCHAR(N)**
> - Text variable
> - N is amount of chars(size of varchar, lenght of the word)
> - VARCHAR(3): word built form 3 chars (egg, koi, BMW, six)

***
