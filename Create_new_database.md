## MySQL Database create new user account with password

- Access mysql database

```bash
sudo mysql
```

- create new alter user account

```bash
alter user 'root'@'localhost' identified with mysql_native_password by 'Rabiussunny32463
542653423#323re'
```

```bash
exit
```

- More security

```bash
mysql_secure_installation
```

### configuration all then follow this command

` login mysql

```bash
sudo mysql -u root -p
```

- create database

```bash
create database exampleDB;
```

- show shemas

```bash
show schemas;
```

- create new user

```bash
create user 'name'@'localhost' identified with mysql_native_password by 'your-password';
```

- use database

```bash
use mysql;
```

- show schema

```bash
select user from user;
```

- access root database

```bash
grant all on exampleDB.* to 'name'@'localhost';
```

- Exit

```bash
exit
```
