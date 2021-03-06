# SECDataParseVBA
Download and query SEC XBRL tags from quarterly and annual financial data

<b>Purpose</b>
Access XBRL data from UDF's within excel.

Note that this project bypasses having to access a web api, and effeciently sets up your own database. The benefits are that data can be accessed without limits of size or number of requests. The downside of course is that we must setup the database. With the classess the database setup should take no longer than 20 to 30 minutes including time to load. 

<b>Project progress:</b>
Classes to build:
<br>
(1) Download SEC Data Class (Complete)
<br>
(2) Load SQL Data Class (50%)
<br>
(3) Query SQL Data Class (10%)
<br>
(4) XBRL taxonomy integration (not started)


<b>Requirements:</b>
<br>
SQL Server (2017) and related driver: msoledbsql_18.1.0.0_x64.msi(or msoledbsql_18.1.0.0_x84.msi)
<br>
Note: Late binding is utilized throughout the class modules, and as such no direct references to libraries need to be made in the VBA interface.

<b>Instructions:</b>
<br>
<b>(1)</b> Place the classes into a VBA project
<br>
<b>(2)</b> Download SQL Server and the msi file for the ability to work with SQL server from VBA
<br>
<b>(3)</b> Place "SECVba" file at the C:\ directory"
<br>
<b>(4)</b> Use the class methods in a module to download SEC data, create SQL Server tables, and load the tables for the data you've downloaded. 
<br>
Note: It's highly suggested you include data validation of some sort for your loads. For example, after loading Q3'2018 num tables you should note that somewhere either as a record in a SQL table, or a sheet in excel. Purpose of this is to ensure you don't load duplicates. 



Example use to instantly query array of data into excel from SQL server (current assets for selected SEC filers as of 20180331):
![alt text](https://github.com/dylan1218/SECDataParseVBA/blob/master/ExampleArrayResult.PNG)
