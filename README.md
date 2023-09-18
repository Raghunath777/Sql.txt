# Sql.txt
# All_Commands

1. *****/*Write an Anonymous block of code in PLSQL ?*/*****

2. *****/***What is the issue with the code ?***/*****
Set SERVEROUTPUT ON;
DECLARE 
	V_TEXT Varchar2(50) NOT NULL;
BEGIN 
	DBMS.OUTPUT.PUT_LINE(V_TEXT);
END;

3. *****/***What is the O/P of this code snippet ?***/*****
Set SERVEROUTPUT ON;
DECLARE 
	V_TEXT Varchar2(50) NOT NULL DEFAULT 'Hello World';
BEGIN 
	v_TEXT := 'PL/SQL' ||"You have get it correct!";
	DBMS.OUTPUT.PUT_LINE(V_TEXT);
END;

4. *****/***Create a table that automatically updates***/*****
TimeStamp and Session Log information of Employee from the Attedance_Table  

(Create Attendance_Table with following columns
EMP ID(Check in Emp Table if the user exists),
Manager ID(Check in User if the Employee exists and Role of Employee = "Manager"),Last Login TimeStamp


create stored procedure which will display EMP_ID, NumberofDays_inactive_from_Lastlogin)

5. *****/*** Case Expression***/*****

create a function that does the case by case evaluation based on the Employee Designation and group's these employee by their Designation 
and update thier Sal with 10%(for SDE),7%( For SDM and SSDM), 5%(for architect and Director) INCREMENT

Sample Input Data 

Emp_ID Emp_Name Emp_Designation Monthly_Emp_Sal
1      Ramesh   SDE - 1         65000 
2	   Suresh   SDE - III       90000
3	   Aditi    SDE - II 		77000
4	   Vishnu   SDM             120000
5      Surya    SSDM            140000
6      Chris	Architect       150000
7	   Abdul    Director        220000


Sample Output 
Emp_ID Emp_Name Emp_Designation Monthly_Emp_Sal INCREMENT SAL_After_Increment
1      Ramesh   SDE - 1         65000            10%          71,500
2	   Suresh   SDE - III       90000            10%          99,000
3	   Aditi    SDE - II 		77000            10%          84,700
4	   Vishnu   SDM             120000            7%          1,28,400 
5      Surya    SSDM            140000            7%          1,49,800
6      Chris	Architect       180000			  5%          1,89,000
7	   Abdul    Director        220000            5%          2,31,000  

*/

6. /***Stored procedure***/
Create Stored procedure that would truncate top 3 tables with maximum number of records greater than 1000;
[not required to create tables, just create a store proc alone]

7. /*** PACKAGE ***/
Create 5 Tables with following names and Add new rows to each of these Five Tables based as and when the package being called.

[You can use different SQL Objects to insert records like a store proc/functions/ simple Insert should also work].


8. /*** Loop / Nested Loops ***/ 
create a Table of tables and Indentify number of columns in each table and print it output along with Table name

Sample Input 
"Table of table" is the table name
Schema 	Table_Name        Table_desc 		
REF 	Users 	          User related information will be available 
CTRL 	Batch		      Batch ctrl information will be available
Layer1	User_Transaction  User_Bank Transaction 

REF - users Table - column names
REF_ID INT 
USER_ID INT
USER_NAME VARCHAR(255)
Status    Char

CTRL Batch Table  - columns
CTRL_ID INT
Batch_ID - INT 
Batch_Start_Date - DateTime
Batch_END_DATE   - DateTime

Layer1 User_Transaction
User_ID  - INT
REF_ID   - INT
USER_TRANSACTION Number
USER_BANK        VARCHAR(255)
USER_BANK_IFSC   VARCHAR(255)
USER_TRANS_Date  DateTime
Batch_Start_Date - DateTime
Batch_END_DATE   - DateTime


9 . *****/***  Triggers  ***/*****
Write a program to create a row level trigger for the CUSTOMERS table that would fire for INSERT or UPDATE or DELETE operations performed on the CUSTOMERS table. 

Notes : 
Write Loop for inserting New_Salary = [Old Salary + 36/100(Old_Salary)]
This trigger will display the salary difference between the old values and new values.


sample Input:
ID	NAME	AGE	ADDRESS	    OLD_SALARY  NEW_Salary
1	Ramesh	23	Allahabad	20000       
2	Suresh	22	Kanpur	    22000
3	Mahesh	24	Ghaziabad	24000
4	Chandan	25	Noida	    26000
5	Alex	21	Paris	    28000
6	Sunita	20	Delhi	    30000

10. *****/***  Cursors  ***/*****




11. *****/***  Dynamic PL/BLOCKS ***/*****
Write a dynamic block of code by declaring a one block of code and assigning it to variable in different block of code and execute the declared variable; 
The task is to print First_name and Last_name of all users in the Emp Table.

Note: - Dynamic block code should not have any parameterized value, should be dynamic when it runs.


12. ***********/**** Write Input from a File  and print the output in SQL developer screen******/********
create a directory in your local machine and read the file using PLSQL UTL package and print all the records iteratively in SQL Developer output.


13. ***********/**** Write Output to a File  ******/********
Create a Stored Procedure to calculate the new salary of the employees and print the out to new directory created in .CSV/.txt format 

Input 
ID	NAME	AGE	ADDRESS	    OLD_SALARY  NEW_Salary
1	Ramesh	23	Allahabad	20000       
2	Suresh	22	Kanpur	    22000
3	Mahesh	24	Ghaziabad	24000
4	Chandan	25	Noida	    26000
5	Alex	21	Paris	    28000
6	Sunita	20	Delhi	    30000

14. Explore Copy, Rename, Remove and Drop file commands in PLSQL.

you may take a particular directory of your choise and perform Copy, Rename, Remove, Drop those files in the that local Directory.
