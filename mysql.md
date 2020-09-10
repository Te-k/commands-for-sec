# MySQL

**Connect**:
```
mysql -u root -p
```

**List databases:**
```
show databases ;
```

**Use a database:**
```
use DATABASE;
```

**List tables:**
```
show tables;
```

**List users:**
```
SELECT User FROM mysql.user;
```

**Create user and grant access to a db:**
```
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
```
