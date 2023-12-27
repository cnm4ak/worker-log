# worker-log
打工人

## MySQL 忘记密码
```bash
1. Stop MySQL server 
2. 在 mysqld.conf 追加一行

   [mysqld]
   skip-grant-tables

3. Start MySQL server

# 5.7
FLUSH PRIVILEGES;
UPDATE mysql.user SET authentication_string = PASSWORD('MyNewPass') WHERE User = 'root' AND Host = 'localhost';

# 8.0
FLUSH PRIVILEGES;
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
```
