# Basic operations of Postgresql

## 1. Select statement

```sql
SELECT column_name FROM table_name;

-- To select multiple column at once

SELECT col1,col2 FROM table_name;
```

## 2. Select distinct

This helps to get unique value from a list of repetating values

```sql
SELECT DISTINCT column_name FROM table_name;

-- to select multiple column or to make it readable add a parathesis

SELECT DISTINCT(col1,col2) FROM table_name;
```
## 3. Count

This helps to count the number of values in a column

```sql
SELECT COUNT(col_name) FROM table_name;

-- To count the number of unique values from a column

SELECT COUNT(DISTINCT(column_name)) FROM table_name';
```
## 4. WHERE

This helps to add conditional statement to our query

```sql
SELECT column_name FROM table_name WHERE your_condition;
```

we can use logical operators like other programming languages

`To add multiple condittion we can use AND, OR, NOT keywords`

## 5. Order By

To order or sort a result ascending or descending order according to a column

```sql
SELECT column1,column2 FROM table_name ORDER BY column1 ASC/DESC

-- To sort through multiple column

SELECT column1,column2 FROM table_name ORDER BY column1,column2 ASC/DESC

-- ASC is applied by default
```

## 6. LIMIT

To limit the number of rows returned by a query, we use limit keyword

```sql
SELECT column_name FROM table_name
WHERE some_condition
ORDER BY column_name
LIMIT some_interger;

-- here some_integer should equal to the number of rows we require in the result
```

## 7. Between 
It select the values between the given parameters inclusive the limits.

We can also use `NOT BETWEEN` statement which gives values exclusive the limits.

```sql
-- The value returned here is including limit1 and limit2

SELECT * FROM table_name WHERE column_name BETWEEN limit1 AND limit2;

-- The value retured here is exclusive of the limit1 and limit2

SELECT * FROM table_name WHERE column_name NOT BETWEEN limit1 AND limit2;
```

## 8. IN

It gives the rows which satisfy the values given in the query for a specific column

```sql
SELECT * FROM table_name
WHERE column_name IN (value1, vakue2, value3, ...);

-- If the value of any row of the given column equal to values given in paranthesis then the row satisfy the query

-- We can also pair IN operator with NOT

SELECT * FROM table_name 
WHERE column_name NOT IN (value1, value2, value3, ...);
```
## 9. LIKE and ILIKE

These queries are helpful for pattern matching of strings in a column.

There are two wildcards.

- `_` : Which means a single character
- `%` : Which means multiple character

```sql
-- for example, if you want to get all the names start with "A", then 

SELECT * FROM table_name
WHERE name_column LIKE 'A%';

-- remember that like is case sensitive while ILIKE is case insensitive

-- To query a string from a column which has a dynamic character (like a version number)

SELECT * FROM table_name 
WHERE varsion LIKE 'version_';

-- This matches with version1, version2, version3 etc


```
