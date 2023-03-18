## docker-compose.yml

```yml
version: "3"

services:
  db:
    image: mariadb:10
    ports:
      - 3306:3306
    volumes:
      - ./db/conf.d:/etc/mysql/conf.d
      - ./db/data:/var/lib/mysql
      - ./db/initdb.d:/docker-entrypoint-initdb.d
    env_file: .env
    environment:
      TZ: Asia/Seoul
    networks:
      - backend
    restart: always

networks:
  backend:
```

## my.cnf

```cnf
[client]
default-character-set = utf8mb4

[mysql]
default-character-set = utf8mb4

[mysqld]
character-set-client-handshake = FALSE
character-set-server           = utf8mb4
collation-server               = utf8mb4_unicode_ci
```

## .env
```env
MYSQL_HOST=localhost
MYSQL_PORT=3306
MYSQL_ROOT_PASSWORD=password
MYSQL_DATABASE=project
MYSQL_USER=user
MYSQL_PASSWORD=password
```