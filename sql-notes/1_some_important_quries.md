# Some important but powerful queries

## Create a table

```sql
CREATE TABLE cities (
  name VARCHAR(50),
  country VARCHAR(50),
  population INTEGER,
  area INTEGER
);
```

## Insert data into the table

```sql
INSERT INTO cities (name, country, population, area)
VALUES ('Tokyo','Japan',23233445, 345232);
```

`Batch insert way`

```sql
INSERT INTO cities (name, country, population, area)
VALUES
	('Tokyo','Japan',33445, 345232),
    ('Delhi','India',943434, 34342),
    ('Shanghai','China',8678678, 23123);
```

## Read Data

```sql
SELECT * FROM cities;
SELECT name, area FROM cities;
```

## Apply matematical operation in the query

```sql
SELECT name, population / area FROM cities;
```

`Give the new coulumn a name using AS keyword`

```sql
SELECT name, population / area AS density FROM cities;
```

## String operation in query

```sql
SELECT name || population / area AS density FROM cities;
SELECT name ||country AS location FROM cities;
SELECT name ||', ' || country AS location FROM cities;
SELECT CONCAT(name,country) AS location FROM cities;
SELECT CONCAT(name,', ',country) AS location FROM cities;
SELECT UPPER(CONCAT(name,', ',country)) AS location FROM cities;
```
