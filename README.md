# What Is JDBC


> JDBC . Java Database Connectivity.


> is a standard Java API for database-independent connectivity between the Java programming language and a wide range of databases.


> The JDBC library includes APIs  

    - Making a connection to a database.
    - Creating SQL or MySQL statements.
    - Executing SQL or MySQL queries in the database.
    - Viewing & Modifying the resulting records.
    
    
> JDBC is a specification that provides a complete set of interfaces that allows for portable access to an underlying database. 
Java can be used to write different types of executables, such as −
 
    - Java Applications
    - Java Applets
    - Java Servlets
    - Java ServerPages (JSPs)
    - Enterprise JavaBeans (EJBs).
 
 
> The JDBC API uses a driver manager and database-specific drivers 
    
    to provide transparent connectivity to heterogeneous databases.
    The JDBC driver manager ensures that the correct driver is used to access each data source. 
    The driver manager is capable of supporting multiple concurrent drivers 


> JDBC Architecture

    Application -> JDBC -> Driver -> DB

    - Java code calss JDBC library
    - JDBC loads a driver
    - Driver can find a particular database

# 7 Steps 
   
    
    1. Load the driver
    2. Define the connection URL
    3. Establish the connection
    4. Create a statement object
    5. Execute a query using the statement
    6. Process the result
    7. close the connection
    
# Common JDBC Components
 
> DriverManager: 

This class manages a list of database drivers. 
Matches connection requests from the java application with the proper database driver using communication sub protocol. 
The first driver that recognizes a certain subprotocol under JDBC will be used to establish a database Connection.

> Driver: 

This interface handles the communications with the database server. You will interact directly with Driver objects very rarely. Instead, you use DriverManager objects, which manages objects of this type. It also abstracts the details associated with working with Driver objects.

> Connection: 

This interface with all methods for contacting a database. The connection object represents communication context, i.e., all communication with database is through connection object only.

> Statement: 

You use objects created from this interface to submit the SQL statements to the database. Some derived interfaces accept parameters in addition to executing stored procedures.

> ResultSet:

These objects hold data retrieved from a database after you execute an SQL query using Statement objects. It acts as an iterator to allow you to move through its data.

> SQLException: 

This class handles any errors that occur in a database application.

  - getSQLState() : return 5 characters for SQL State Value   ex)42Y55
  - getErrorCode() : return integer value representing the error code   ex) 30000
  - printStackTrace() : standardized and generated automatically

