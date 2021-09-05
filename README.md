# SQL Tutorials

Hello!

Here are some SQL tutorials I've been creating and posting to Twitter.

I've first written a brief intro to databases. Following from that, there's a series of small SQL tutorials.

If you find any of this useful, consider supporting me at [BuyMeACoffee](https://www.buymeacoffee.com/AbzAaron) :-D

## What is a database?

This is essentially a container storing organised data electronically, usually controlled by something called a database management system (DBMS for short). These can store more data (and are more secure) than a text file or spreadsheet.

## What is a DBMS?

These are software packages which allow us to create, manipulate and manage our databases. You've probably heard of some before.

They include:

* MySQL
* SQLite
* PostgreSQL

## What is a table?

These are structured files containing data within the database. Typically, a database contains multiple tables, each composed of rows & columns. This makes data retrieval easier.

## What are table columns & rows?

Picture tables like spreadsheets. We have columns storing a particular type of data, such as name, price, or date, with each row representing a specific record.

## What is a type of data?

Each column in a table has a datatype. A column called age would be a numeric datatype, as an example. Setting datatypes correctly can:

* Restrict incorrect data being inserted
* Help if data needs to be sorted
* Help optimise memory usage

## What are constraints?

These are rules enforced on your data, ensuring the correct type of data is entered into a database, maintaining data integrity. For example, a UNIQUE type constraint would ensure all values in a table column remain unique.

## What is a primary key?

This is a column or combo of columns designed to uniquely identify each table row. Without a primary key, we won't always be able to uniquely identify a table record. An example might be a 'user_ID' column, whereby each record has its own unique ID.

## What is a foreign key?

This is a column or combo of columns in a table that refers to the primary key of another table. This establishes a link between tables, allowing us to join them together if required. 

## What is SQL?

SQL, or Structured Query Language, is what we use to communicate with databases. We use this to remove data, add data, read data, join tables, create tables, and so on. It's easy to learn, and almost all DBMS support SQL. So it's worthwhile learning this!

## Getting Started

A good place to get started is with SQLite. Follow the below steps to get set-up:

1. Download **DB Browser for SQLite** from https://sqlitebrowser.org
2. Download the [Chinook sample database](chinook.db)
3. Open up DB Browser for SQLite and open the database
4. Under the *Database Structure* tab, you can see a list of tables
5. Under the *Execute SQL* tab, you can run SQL queries

Alternatively, you can use the SQLite command line program, rather than DB Browser:
https://www.sqlite.org/cli.html

You can view the database diagram illustrating table relationships for the Chinook database here:
https://www.sqlitetutorial.net/sqlite-sample-database/

Play around with this database as you read through some of these tutorials. You can start by simply typing a basic command and running it to see the output:

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/db_browser.png">

## Select Statment

The `SELECT` statement is used to retrieve table data. We only need to specify what we want to select and where we want to select it from. Simple!

Note that we use `FROM` to specify the table we wish to retrieve data from.

In the below example, you'll notice we've used the * character. This signifies that we want to return all columns in the table. This is useful when you are practicing; however, it's bad practice within a real production enviornment, and can slow things down. Rarely would we ever need to retun all columns.

Additionally, pay attention to column placement when we are returning more than one column. There should be a comma between each column name, but not after the last one. If we were to include a comma after the last column in a `SELECT` statment, we would get an error.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Select.png">

## Sorting 

When retrieving data from a table, it will generally be displayed in the order it appears within that table; therefore it's not a good idea to rely on data being in any specific order when retrieving it. Instead, you can explicitly sort using `ORDER BY`.

If we want to order descendingly, we can use `DESC`. We can also explicity write `ASC` for ascending. However, as this is the default, we don't really need to include it.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Sort.png">

## Where Clause

When extracting data from tables, you'll normally only want a subset of the data. Achieve this using the `WHERE` clause, which will filter the data.

Specify `WHERE` after the `FROM` clause.

Note that we've split our queries across multiple lines here, rather than just writing it all on a single line. In SQL, we don't have to worry about whitespace. It's usually good practice to split long queries across multiple lines for better readability.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Where.png">

## Where Clause ~ Part 2

We can combine `WHERE` clauses with `AND` or `OR`.

When combining these operators, `AND` is processed before `OR`. 

But... we can control evaluation order using parentheses to explicitly group operators, a bit like what we do in Maths! For example:

* 5 + 2 x 3 = 11
* (5 + 2) x 3 = 21

Note how we use parenthese to change the order of evaluation, and thus change the final result. We can do the same with `AND` and `OR` in SQL.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Where2.png">

## Wildcards ~ Percent ( % )

Wildcards are symbols used to substitute characters within a text string. Adding these to a search condition allows us to filter data matching a pattern. 
 
To do this, we use the `LIKE` operator within a `WHERE` clause.

Let's look at the % wildcard.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/WC-Percent.png">

## Wildcards ~ Underscore ( _ )

Another wildcard is the underscore.

This matches 1 character, differing from the % wildcard, which represents 0, 1, or more characters.

Note: wildcard searches typically take longer to run, especially if wildcard is at the start of a search pattern. Consider this before using. 

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/WP-Underscore.png">

## Calculated Fields ~ Concatenation

In a `SELECT` statement, we can *calculate* new columns on-the-fly without altering the database data itself.

One example is *concatenating* columns together.

To give a new field a proper name, we use the `AS` keyword. Note that we don't actually have to include the `AS` keyword. The query would work exactly the same if we omitted this. However it's good practice to include it, for readability.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Concat.png">

## Calculated Fields ~ Maths

We learned we can calculate fields on-the-fly without altering database data itself

One use for this is concatenation. Another is running maths operations on retrieved data.

Here are some operators:

* Division ( / )
* Addition ( + )
* Subtraction ( - )
* Multiplication ( * )

If we want to change the order or precedence, we can use parentheses (like we would in Maths).

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Maths.png">

## Functions ~ Part 1

Functions are a set of instructions grouped together, used to perform a specific task. 

Value(s) can be passed to a function, which the function then operates on.

This can make manipulating or converting data in SQL simpler and more efficient.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Functions1.png">

## Additional Info

Here's just a bit more information on SQL statements!

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/tips.png">

## Aggregate Functions

Aggregate functions run calculations on a set of rows to return a single value. These are:

1. `MAX`
1. `MIN`
1. `AVG`
1. `SUM`
1. `COUNT`

These all ignore `NULL` (blank) values except for `COUNT(*)` which counts the number of table rows.

We can use `DISTINCT` to include only unique values. Notice how it changes the average returned when we use this.

Note that where you see `DISTINCT` below, you could replace this with `ALL` to perform the calculation on all rows. However, we would never do this, as `ALL` is actually the default. 

So for example, we could rewrite one of the other lines, like `SUM(price) AS sum_price`, as `SUM(ALL price) AS sum_price` instead. This would do exactly the same thing.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/aggregate.png">

## Grouping Data

The `GROUP BY` clause creates a separate group for each unique value in a column or set of columns.

We can then perform aggregate functions like `SUM` or `AVG` on each individual group.

Note that, if a grouping column contains `NULL`, this will be classed as a group. Also, `GROUP BY` can list multiple columns to group by (each of these must be a retrieved column under the `SELECT` statement except for the aggregate function). Similarly, every column listed in the `SELECT` statement must be included in the `GROUP BY` clause; again, with the exception of the aggregate function(s).

Finally, `GROUP BY` comes after the `FROM` clause and `WHERE` clauses, but before the `ORDER BY` clause.

It's worth playing around with this on your own so you can better understand what's going on.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/group_by_1.png">

## Filtering Grouped Data

We use `HAVING` to filter grouped data. This is very similar to the `WHERE` clause.

Only difference is `WHERE` filters specific rows (filters before data is grouped) and `HAVING` filters groups (filters after data is grouped)

Note: We can use both clauses in one statement. So for example, we might want to filter our data using `WHERE`, then group the data, and filter those groups usin `HAVING`.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Having.png">

## Subqueries

A *subquery* is an SQL query embedded within another query, often used within `WHERE` clause `IN` operators

Subqueries are processed starting with the innermost `SELECT` statement

Note: although powerful, subqueries can negatively impact performance. There are other ways we can perform the type of data retrieval we are conducting here (more on that in a later tutorial).

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/subqueries.png">

## Subqueries ~ Part 2

Not always the best option, but we can use *subqueries* to create calculated fields (columns created on-the-fly) within a `SELECT` statement. 

Note: Because both tables below contain an "em_id" column, we've used syntax "table.column" to remove ambiguity & ensure correct results (i.e. Employees.em_id and Expenses.em_id).

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/subqueries-CF.png">



