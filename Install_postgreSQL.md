## Install and configure PostgreSQL and pgadmin

- Import the repository signing key

```bash
sudo apt install curl ca-certificates
```

```bash
sudo install -d /usr/share/postgresql-common/pgdg
```

```bash
sudo curl -o /usr/share/postgresql-common/pgdg/apt.postgresql.org.asc --fail https://www.postgresql.org/media/keys/ACCC4CF8.asc
```

- Create the repository configuration file

```bash
sudo sh -c 'echo "deb [signed-by=/usr/share/postgresql-common/pgdg/apt.postgresql.org.asc] https://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

```

- Update the package lists

```bash
sudo apt update
```

- Install the latest version of PostgreSQL

```bash
sudo apt install postgresql-17
```

- check version

```bash
sudo su - postgres
psql
select version();
```

- see users

```bash
\du
```

- add new user

```bash
alter user name with password 'your_password'
```

- see database

```bash
\l
```

- create new database

```bash
create database my_database
```

- show database

```bash
\l
```

- create new user

```bash
create user name with password 'your_password'
```

- conect database

```bash
\c name
```
