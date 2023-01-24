# Unit 2: Generate Code

## Structured Query Language (SQL)
> SQL is a standard language for storing, manipulating and retrieving data in databases {cite}`w3schools_2019_sql`.

SQL is the the most popular language for working with databases despite being over 50 years old. It is everywhere and every major IT platform uses it. Why? Because it is powerful and effective.

### SQLite
There are many different flavours of SQL. Most of these work by setting up an SQL server separate from the computer running the program. We will be using SQLite as our SQL database. It is a lightweight and fast database management system, which can run off a file stored on your local machine.

### SQL Tutorials
Below are links to tutorials to refresh your knowledge on the SQL we will use in this course.

#### Retrieving Data
**Basic Queries**
- **<a href="https://www.w3schools.com/sql/sql_select.asp" target="_blank">SELECT Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_alias.asp" target="_blank">Aliases</a>**
- **<a href="https://www.w3schools.com/sql/sql_distinct.asp" target="_blank">SELECT DISTINCT Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_where.asp" target="_blank">WHERE Clause</a>**
- **<a href="https://www.w3schools.com/sql/sql_and_or.asp" target="_blank">AND, OR, NOT Operators</a>**
- **<a href="https://www.w3schools.com/sql/sql_null_values.asp" target="_blank">NULL Values</a>**
- **<a href="https://www.w3schools.com/sql/sql_top.asp" target="_blank">LIMIT Clause** (use the MySQL syntax)</a>
- **<a href="https://www.w3schools.com/sql/sql_orderby.asp" target="_blank">ORDER BY Keyword</a>**
- **<a href="https://www.w3schools.com/sql/sql_operators.asp" target="_blank">Arithmetic Operators</a>**
- **<a href="https://www.w3schools.com/sql/sql_like.asp" target="_blank">LIKE Operator</a>**
- **<a href="https://www.w3schools.com/sql/sql_wildcards.asp" target="_blank">Wildcard Characters</a>**
- **<a href="https://www.w3schools.com/sql/sql_between.asp" target="_blank">BETWEEN Operator</a>**

**Aggregation**
- **<a href="https://www.w3schools.com/sql/sql_min_max.asp" target="_blank">MIN() and MAX() Functions</a>**
- **<a href="https://www.w3schools.com/sql/sql_count_avg_sum.asp" target="_blank">COUNT(), AVG() and SUM() Functions</a>**
- **<a href="https://www.w3schools.com/sql/sql_groupby.asp" target="_blank">GROUP BY Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_having.asp" target="_blank">HAVING Clause</a>**

**Joins**
- **<a href="https://www.w3schools.com/sql/sql_join.asp" target="_blank">JOIN</a>**
- **<a href="https://www.w3schools.com/sql/sql_join_inner.asp" target="_blank">INNER JOIN Keyword</a>**
- **<a href="https://www.w3schools.com/sql/sql_join_left.asp" target="_blank">LEFT JOIN Keyword</a>**
- **<a href="https://www.w3schools.com/sql/sql_join_right.asp" target="_blank">RIGHT JOIN Keyword</a>**
- **<a href="https://www.w3schools.com/sql/sql_join_full.asp" target="_blank">FULL OUTER JOIN Keyword</a>**
- **<a href="https://www.w3schools.com/sql/sql_join_self.asp" target="_blank">Self Join</a>**

**Sub-queries**
- **<a href="https://www.w3schools.com/sql/sql_in.asp" target="_blank">IN Operator</a>**
- **<a href="https://www.w3schools.com/sql/sql_exists.asp" target="_blank">EXISTS Operator</a>**


#### Create Tables and Modify Data
**Database Management**
- **<a href="https://www.w3schools.com/sql/sql_create_db.asp" target="_blank">CREATE DATABASE Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_drop_db.asp" target="_blank">DROP DATABASE Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_create_table.asp" target="_blank">CREATE TABLE Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_drop_table.asp" target="_blank">DROP TABLE Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_alter.asp" target="_blank">ALTER TABLE Statement</a>**
- **<a href="https://www.w3schools.com/sql/sql_notnull.asp" target="_blank">NOT NULL Constraint</a>**
- **<a href="https://www.w3schools.com/sql/sql_unique.asp" target="_blank">UNIQUE Constraint</a>**
- **<a href="https://www.w3schools.com/sql/sql_primarykey.asp" target="_blank">PRIMARY KEY Constraint</a>**
- **<a href="https://www.w3schools.com/sql/sql_foreignkey.asp" target="_blank">FORIEGN KEY Constraint</a>**
- **<a href="https://www.w3schools.com/sql/sql_autoincrement.asp" target="_blank">AUTO INCREMENT Field</a>**

**Data Management**
- **<a href="https://www.w3schools.com/sql/sql_insert.asp" target="_blank">INSERT INTO Statement</a>**
**<a href="https://www.w3schools.com/sql/sql_update.asp" target="_blank">UPDATE Statement</a>**
**<a href="https://www.w3schools.com/sql/sql_delete.asp" target="_blank">DELETE Statement</a>**

## SQL & Python

This section gives a brief overview of using SQLite in Python. W3schools give more details in **[this blog](https://www.w3schools.blog/sqlite-tutorial)**.

To work with SQLite in Python we will use the `sqlite3` module. It is part of the Python standard Library, so it is already installed.

### Setup
There are three steps to setting up your Python code to use `sqlite3`:
#### 1. Import the module
This is your usual `import` command at the top of your Python file.

``` python
import sqlite3
```
#### 2. Connect to the database
You need to create a connection object. The connection object is used to make changes to the database file. Generate a connection object using the `sqlite3.connect` method and assign it to a variable.

``` python
import sqlite3

connection = sqlite3.connect("database_file.db")
```

#### 3. Create a cursor
Finally you need to create a cursor object. The cursor object is used to run SQL queries on the database via the connection object.

``` python
import sqlite3

connection = sqlite3.connect("database_file.db")
cursor = connection.cursor()
```

Now you are set to access your SQLite database with Python.

### Queries

There are two steps to running a query in using `sqlite3` and Python.

#### 1. Execute the SQL query statement
The SQL query statement is provided as a string. Below is an example of how I format the code using a multiline string. It makes it easier to read, and, therefore, increases maintainability.

``` python
cursor.execute(
    """
    SELECT name, phone_num
    FROM customers
    """
)
```

#### 2. Fetch the results
Once the query has been executed, you need to fetch the results that are stored in the cursor. You have three fetching options:
1. `fetchall()` - returns all the results
2. `fetchone()` - returns the next result
3. `fetchmany(size)` - returns the `size` number of rows 

``` python
cursor.execute(
    """
    SELECT name, phone_num
    FROM Customers
    """
)

reults = cursor.fetchall()
```

### INSERT, CREATE, UPDATE, DELETE
All SQL statements that involve making changes to the database (INSERT, CREATE, UPDATE and DELETE) also have two steps, but they are slightly different.

#### Execute the SQL statement
The first step in as the same. The cursor needs to be used to execute the SQL statement.

``` python
import sqlite3

cursor.execute(
    """
    INSERT INTO Customers (name, phone_num)
    VALUES ("John", "0434123456")
    """
)
```

#### Commit changes
The changes to the database will not be permanent until they have been committed to the database file. You can commit numerous execute commands to the database in one go. To make the commitment we use the connection's `commit()` method.

``` python
import sqlite3

cursor.execute(
    """
    INSERT INTO Customers (name, phone_num)
    VALUES ("John", "0434123456")
    """
)

connection.commit()
```

### Using variables

![XKCD](https://imgs.xkcd.com/comics/exploits_of_a_mom.png)

To avoid SQL injection attacks, the correct way to insert variables values into your SQL statements is to use the parameter substitution method. This method inserts a placeholder in the SQL statement, and the values are then passes as a second argument to the `execute()` method. We will be using dictionaries to do this, although lists can also be used.

#### Queries
Below is an example of a parameterised query statement.

``` python
import sqlite3

cursor.execute(
    """
    SELECT name, phone_num
    FROM Customers
    WHERE name = :name
    """,
    {
        "name": "John"
    }
)

reults = cursor.fetchall()
```

#### INSERT, CREATE, UPDATE, DELETE

Below is an example of a parameterised insert statement

``` python
import sqlite3

cursor.execute(
    """
    INSERT INTO Customers (name, phone_num)
    VALUES (:name, :phone)
    """,
    {
        "name":"John",
        "phone":"0434123456"
    }
)

connection.commit()
```