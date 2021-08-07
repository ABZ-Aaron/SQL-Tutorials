# SQL Tutorials

Some SQL tutorials I've been creating and posting to Twitter :)

### Select Statment

The SELECT statement is used to retrieve table data. We only need to specify what we want to select and where we want to select it from. Simple!

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/Select.png">

### Sorting 

When retrieving data from a table, it'll generally be displayed in the order it appears within that table. You can explicitly sort using ORDER BY.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/Sort.png">

### Where Clause

When extracting data from tables, you'll normally only want a subset of the data. Achieve this using the WHERE clause, which will filter the data.

Specify WHERE after the FROM clause.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/Where.png">

### Where Clause ~ Part 2

We can combine WHERE clauses with AND or OR.

When combining these operators, AND is processed before OR. 

But... we can control evaluation order using parentheses to explicitly group operators, a bit like what we do in Maths!

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/Where2.png">

### Wildcards ~ Percent ( % )

Wildcards are symbols used to substitute characters within a text string. Adding these to a search condition allows us to filter data matching a pattern. 
 
To do this, we use the LIKE operator within a WHERE clause.

Let's look at the % wildcard.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/WC-Percent.png">

### Wildcards ~ Underscore ( _ )

Another wildcard is the underscore.

This matches 1 character, differing from the % wildcard, which represents 0, 1, or more characters.

Note: wildcard searches typically take longer to run, especially if wildcard is at the start of a search pattern. Consider this before using.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/WP-Underscore.png">

### Calculated Fields ~ Concatenation

In a SELECT statement, we can *calculate* new columns on-the-fly without altering the database data itself.

One example is *concatenating* columns together.

To give a new field a proper name, we use the AS keyword.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/Concat.png">

