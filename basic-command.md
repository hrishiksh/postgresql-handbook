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

## Database basic operation

- Create a database

  `postgres=# CREATE DATABASE <databasename>;`
