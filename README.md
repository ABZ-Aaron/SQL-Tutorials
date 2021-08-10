# SQL Tutorials

Some SQL tutorials I've been creating and posting to Twitter :)

### Select Statment

The **SELECT** statement is used to retrieve table data. We only need to specify what we want to select and where we want to select it from. Simple!

Note that we use **FROM** to specify the table we wish to retrieve data from.

In the below example, you'll notice we've used the * character. This signifies that we want to return **all** columns in the table. This is useful when you are practicing; however, it's bad practice within a real production enviornment, and can slow things down. Rarely would we ever need to retun all columns.

Additionally, pay attention to column placement when we are returning more than one column. There should be a comma between each column name, but **not** after the last one. If we were to include a comma after the last column in a SELECT statment, we would get an error.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Select.png">

### Sorting 

When retrieving data from a table, it will generally be displayed in the order it appears within that table; therefore it's not a good idea to rely on data being in any specific order when retrieving it. Instead, you can explicitly sort using ORDER BY.

If we want to order descendingly, we can use DESC. We can also explicity write ASC for ascending. However, as this is the default, we don't really need to include it.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Sort.png">

### Where Clause

When extracting data from tables, you'll normally only want a subset of the data. Achieve this using the WHERE clause, which will filter the data.

Specify WHERE after the FROM clause.

Note that we've split our queries across multiple lines here, rather than just writing it all on a single line. In SQL, we don't have to worry about whitespace. It's usually good practice to split long queries across multiple lines for better readability.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Where.png">

### Where Clause ~ Part 2

We can combine WHERE clauses with AND or OR.

When combining these operators, AND is processed before OR. 

But... we can control evaluation order using parentheses to explicitly group operators, a bit like what we do in Maths! For example:

* 5 + 2 x 3 = 11
* (5 + 2) x 3 = 21

Note how we use parenthese to change the order of evaluation, and thus change the final result. We can do the same with AND and OR in SQL.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Where2.png">

### Wildcards ~ Percent ( % )

Wildcards are symbols used to substitute characters within a text string. Adding these to a search condition allows us to filter data matching a pattern. 
 
To do this, we use the LIKE operator within a WHERE clause.

Let's look at the % wildcard.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/WC-Percent.png">

### Wildcards ~ Underscore ( _ )

Another wildcard is the underscore.

This matches 1 character, differing from the % wildcard, which represents 0, 1, or more characters.

Note: wildcard searches typically take longer to run, especially if wildcard is at the start of a search pattern. Consider this before using. 

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/WP-Underscore.png">

### Calculated Fields ~ Concatenation

In a SELECT statement, we can *calculate* new columns on-the-fly without altering the database data itself.

One example is *concatenating* columns together.

To give a new field a proper name, we use the AS keyword. Note that we don't actually have to include the AS keyword. The query would work exactly the same if we omitted this. However it's good practice to include it, for readability.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Concat.png">

### Calculated Fields ~ Maths

We learned we can calculate fields on-the-fly without altering database data itself

One use for this is concatenation. Another is running maths operations on retrieved data.

Here are some operators:

* Division ( / )
* Addition ( + )
* Subtraction ( - )
* Multiplication ( * )

If we want to change the order or precedence, we can use parentheses (like we would in Maths).

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Maths.png">

### Functions ~ Part 1

Functions are a set of instructions grouped together, used to perform a specific task. 

Value(s) can be *passed* to a function, which the function then operates on.

This can make manipulating or converting data in SQL simpler and more efficient.

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/Functions1.png">

### Additional Info

Here's just a bit more information on SQL statements!

<img src="https://github.com/ABZ-Aaron/SQL-Tutorials/blob/master/images/tips.png">



