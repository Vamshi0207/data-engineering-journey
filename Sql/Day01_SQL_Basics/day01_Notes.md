# Day 1 - SQL Basics
**Source**: https://sqlbolt.com

## Topics Learned

#**What is SQL**
  SQL, or **Structured Query Language**, is a language designed to allow both technical and non-technical users to query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

#**- SELECT**
  To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned.
  If we want to **retrieve absolutely all the columns of data from a table**, we can then use the asterisk (*)
  SELECT * 
  FROM mytable;
  the most basic query we could write would be one that **selects for a couple columns** (properties) of the table with all the rows (instances).
  SELECT column, another_column, …
  FROM mytable;
  
#**- WHERE**
  In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
  SELECT column, another_column, …
  FROM mytable
  WHERE condition
    AND/OR another_condition
    AND/OR …;
  
**#- ORDER BY**
  SQL provides a convenient way to**discard rows that have a duplicate column value by using the DISTINCT keyword**.
  SELECT DISTINCT column, another_column, …
  FROM mytable
  WHERE condition(s);
  SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause.

  SELECT column, another_column, …
  FROM mytable
  WHERE condition(s)
  ORDER BY column ASC/DESC;
  When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text.

## Examples

SELECT * FROM employees;

SELECT name
FROM employees;

SELECT *
FROM employees
WHERE salary > 50000;

## Key Takeaways

- SELECT retrieves data.
- WHERE filters data.
- ORDER BY sorts data.
