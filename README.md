# worker-log
打工人

MySQL修改密码
```bash
# 5.7
FLUSH PRIVILEGES;
UPDATE mysql.user SET authentication_string = PASSWORD('MyNewPass') WHERE User = 'root' AND Host = 'localhost';
FLUSH PRIVILEGES;

# 8.0
FLUSH PRIVILEGES;
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
```
