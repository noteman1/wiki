# MariaDB 무설치 데이터 설정하기

```cmd
mysql_install_db --datadir="C:\project\mariadb-10.11.2-winx64\data" -port=3306 --password=password
mysql_install_db --datadir="C:\project\mariadb-10.11.2-winx64\data" -port=3306 --password=password --service=mariaDB -
```

## MariaDB root 비밀번호 변경

```sql
ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';
flush privileges;
```