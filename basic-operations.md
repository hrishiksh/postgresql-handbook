# Basic operations of Postgresql

## 1. Select statement

```sql
SELECT column_name FROM table_name;

\\ To select multiple column at once

SELECT col1,col2 FROM table_name;
```

## 2. Select distinct

This helps to get unique value from a list of repetating values

```sql
SELECT DISTINCT column_name FROM table_name;

// to select multiple column or to make it readable add a parathesis

SELECT DISTINCT(col1,col2) FROM table_name;
```
