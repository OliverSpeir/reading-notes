# Learn SQL
- [eBook PDF](https://cdn2.hubspot.net/hubfs/392937/Learn%20SQL.pdf?utm_referrer=https%3A%2F%2Flanding.chartio.com%2F)
- [SQLBolt Exercises and Information] (https://sqlbolt.com/)

## Basics
- `*` is called splat and is wildcard
### SELECT
- most common command, gets certain data from the database for viewing
### FROM
- conditional for select, so you would SELECT [value you want to see] FROM [table name]
### ORDER BY
- another conditional for select
- SELECT * FROM tablename ORDER BY column
### LIMIT and OFFSET
- SELECT * FROM tablename LIMIT 5 OFFSET 2
- limit number of results and offset starts to list the results from a certain position
### Browse SCEHMA
- useful to see all the data in a database (tables and such)

## Mid Level SQL

### WHERE
- condtions for search
- SELECT * FROM tablename WHERE conditions
- can use AND OR NOT with WHERE
### PostgreSQL Operators 
- `=`
- `<`
- `>`
- `<=`
- `>=`
- `!=` or `<>` 
- LIKE ILIKE and SIMILIAR TO
- like is case sensitive string match
- ilike is insensetive
- SIMILIAR TO is regex match
### NULLs
- IS NULL 
- IS NOT NULL 
- must use these instead of =0
### Aggregate Functions
- COUNT and COUNT DISTINCT 
- count number of rows that are not NULL and disctinct excludes duplicates
- can give an alias to the data that is returned by AS keyword and doublequotes
- AS "query1" COUNT tablename
### GROUP BY
- groups rows that have the same values into summary rows
- SELECT COUNT(CustomerID), Country FROM Customers GROUP BY Country;
- this will show count of number of customers from a certain country
- if GROUP BY was not included it would just count all the customers
- *this information is from W3 schools*
### JOIN (relationship or table)
- JOIN is useful to get results from multiple tables 
- can either join by a relationship or by table names 
- this section also defines Primary Keys and Foreign Keys here
- Primary key is a column in a table that has unique value for each row
- Foreign key is a column that has a value from another table which creates a relationship
- can JOIN INNER which selects records that have matching values in both tables *from w3 schools*
- can JOIN FULL OUTER, LEFT OUTER, RIGHT OUTER which selects records that match either table or just the 1st or 2nd joined tables
### DATE and TIME functions
- TIMESTAMP returns full date and time in certain format
- DATE returns just date
- TIME returns just time
- INTERVAL used to select records by timestamps, so records every 6 hours for example
- can TO_CHAR to format date nicely
## Extras
### UNION and UNION ALL
- similar to join but combines results from a query not just a table or relationship
- UNION only keeps unique records
- UNION ALL  keeps all including duplicates 
- There must be the same number of columns retrieved in each SELECT statement to
be combined.
- The columns retrieved must be in the same order in each SELECT statement.
- The columns retrieved must be of similar data types.

### Exclude a column
- can either just not select it, SELECT column1, column3
- can comment it out, SELECT column1, --column2, column3
### SQL DESCRIBE
- DESCRIBE tablename
- returns sample table with datatype of each cell and column names
### CREATE VIEW
- makes a virtual table that can be selected from
- CREATE VIEW viewname AS SELECT columnsdesired FROM tablename
### AND OR logic
- AND for multiple conditions
- OR for any of the conditions
- if, if-else are also viable in SQL
### Copying data between tables
- simple as CREATE TABLE copyname AS tanlename WITH NO DATA 
- no data omits the data and just copies the structure
- can insert into pre-existing table with INSERT INTO tabletoinsertinto SELECT columnstocopy FROM table WHERE condtional
### Export with CSV
- For Client-Side Export:
- \copy [Table/Query] to '[Relative Path/filename.csv]' csv header
- For Server-Side Export:
- COPY [Table/Query] to '[Absolute Path/filename.csv]' csv header;
### PostgreSQL generate series of numbers
- generate_series([start], [stop], [{optional}step/interval]);
- can also generate timestamps
### Copy a database in PostgreSQL
- CREATE DATABASE [Database to create] WITH TEMPLATE [Database to copy] OWNER [Your username];
- this doesnt copy the data just the structure
### Export PostgreSQL data to a CSV or Excel file
- COPY [Table Name] TO '[File Name]' DELIMITER ',' CSV HEADER;
### Replace Null with 0s in SQL
- UPDATE [table] SET [column]=0 WHERE [column] IS NULL;
### Importing data from CSV in PostgreSQL
- COPY [Table Name](Optional Columns) FROM '[Absolute Path to File]' DELIMITER '[Delimiter Character]' CSV [HEADER];

### Meta commands in PSQL
- \c [database name] - connect to a specified database
- \l - list all databases
- \d - display tables, views, and sequences
- \dt - display just tables
- \dv - display views
- \dm - display materialized views
- \di - display indexes
- \dn - display schemas
- \dT - display data types
- \sv [view name] - show a views definition
- \x - toggle expanded display. Useful for tables with a lot of columns being accessed *Can be toggled on/off or set to auto*
- \set - list all internal variables
- \set [Name] [Value] - set new internal variable
- \unset [Name] - delete internal variable
- \cd - change the directory that psql is working in
- \! [Command] - execute shell command Ex. \! ls or \! pwd
- \timing - toggles timing on queries
- \echo [message] - print the message to the console
- \copy - copies to a file
- \i [filename] - execute commands from a file
- \o [file] - writes output to file instead of console
- \q - exits psql
- Multiple meta commands can be used in one line. For example you could use \dt\di to
list all tables and then list all indexes with additional technical information on the indexes
### Outputting query results to a file
- ` \o <br> [filename].txt
    [Query or Queries to write to file];
    <br>
    \o `
- output metacommand 
### Generate Random data in PostGreSQL
- random() function
- specific examples provided in eBook
### using ALTER in PostgreSQL
- In SQL, tables, databases, schemas, groups, indexes, servers, and more can be modified using the ALTER command. This command enables the user to modify a specific aspect of the table, database, group, etc. while leaving the rest of the data untouched.

## Screenshots from SQLBolt Exercises
<img src ="https://i.imgur.com/Z3Uzgw5.png"/>
<img src ="https://i.imgur.com/60cRtn6.png"/>
<img src ="https://i.imgur.com/4jVq0G4.png"/>
<img src ="https://i.imgur.com/iHTe3gZ.png"/>
<img src ="https://i.imgur.com/7BXomOY.png"/>
<img src ="https://i.imgur.com/Dy01aYE.png"/>
<img src ="https://i.imgur.com/zm7q9Ar.png"/>
<img src ="https://i.imgur.com/wvx1eZB.png"/>
<img src ="https://i.imgur.com/ngUabHc.png"/>
<img src ="https://i.imgur.com/ZaVPoQI.png"/>
<img src ="https://i.imgur.com/Aa46V5j.png"/>
<img src ="https://i.imgur.com/6hDMAtL.png"/>