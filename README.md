DocRequestLogReport
===================

####Setting up your new database:

Find the two included SQL files:  
**DocumentRequestData_create_database.sql**  
**DocumentRequestData_insert_data.sql**

1. In SQL Server Management Studio, open a new query window, copy the contents of **DocumentRequestData_create_database.sql** into it, and execute it. You will now have an empty database called **DocumentRequestData**.
2. Refresh your list of databases in the Object Explorer to verify that the database was created. Right click on the database and select New Query. Execute **DocumentRequestData_insert_data.sql**. You will now have a table called **RD_RequestLog** populated with plenty of test data to work with. 

Feel free to insert, update, and delete as many records as you would like. 

=======

####Setting up your project: 

Create a new web site project in Visual Studio. In the **web.config** file, add a connection string to the `<connectionStrings>` section to go to your newly created database as such:  

    <connectionStrings>
        <add name="DocRequestLogConnString" connectionString="Data Source=<SQLServerName>;Initial Catalog=DocumentRequestData;UID=<UserName>;PWD=<Password>" />
    </connectionStrings>
