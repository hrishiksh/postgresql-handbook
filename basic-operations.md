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

