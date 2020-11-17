# Basic Commands

- To start a postgresql service

  ```sql
  sudo service postgresql start
  ```

- To stop the service

  ```sql
  sudo service postgresql stop
  ```

- To open psql console

  ```sql
  sudo -u postgres psql
  ```

- To see list of tables inside database

  ```sql
  postgres=# \l
  ```

- To set password

  ```sql
  postgres=# \password
  ```

- To quit psql console

  ```sql
  postgres=# \q
  ```

## Database Create, Connect & Delete

- Create a database

  ```sql
  postgres=# CREATE DATABASE <databasename>;
  ```

- Delete a database

  ```sql
  postgres=# DROP DATABASE <database name>;
  ```

- Connet to a database

  ```sql
  psql -h <hostname> -p <port number> -U <username> <database Name>
  ```

  for example: suppose we have a database named test in localhost. so we have to enter

  ```sql
  psql -h localhost -p 5432 -U postgres test
  ```

  Another way to connect a database using postgres interective terminal (psql) is

  ```sql
  postgres=# \c <database name>
  ```

  for example:

  ```sql
  postgres=# \c test
  ```

## Table operations

- Create a table without constrains (here dbname is your database name)

  ```sql
  dbname=# CREATE TABLE <tablename>(
    <Column name> <datatype>
  )
  ```

  for example, Let's create a person database

  ```sql
  dbname=# CREATE TABLE person(
    id INT,
    firstname VARCHAR(50),
    lastname VARCHAR(50),
    gender VARCHAR(10),
    date_of_birth DATE
  );
  ```

- To list all the table inside a database (or to describe)

  ```sql
  dbname=# \d
  ```

- To describe all the column in a table

  ```sql
  dbname=# \d <tablename>
  ```
