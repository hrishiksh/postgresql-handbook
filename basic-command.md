# Basic Commands

- To start a postgresql service

  `sudo service postgresql start`

- To stop the service

  `sudo service postgresql stop`

- To open psql console

  `sudo -u postgres psql`

- To see list of tables inside database

  `postgres=# \l`

- To set password

  `postgres=# \password`

- To quit psql console

  `postgres=# \q`

## Database Create, Connect & Delete

- Create a database

  `postgres=# CREATE DATABASE <databasename>;`

- Delete a database

  `postgres=# DROP DATABASE <database name>;`

- Connet to a database

  `psql -h <hostname> -p <port number> -U <username> <database Name>`

  for example: suppose we have a database named test in localhost. so we have to enter

  `psql -h localhost -p 5432 -U postgres test`

  Another way to connect a database using postgres interective terminal (psql) is

  `postgres=# \c <database name>`

  for example:

  `postgres=# \c test`
