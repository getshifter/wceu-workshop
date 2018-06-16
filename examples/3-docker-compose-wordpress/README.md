# Docker Compose: WordPress

Docker Compose using WordPress

```
version: '3.3'

services:
 
  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    ports:
      - "8000:80"
    volumes:
      - ./config/php.ini:/usr/local/etc/php/conf.d/php.custom.ini
      - ./app/wp-content:/var/www/html/wp-content
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress
  
  db:
    image: mariadb:latest
    volumes:
      - ./app/db:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

volumes:
    db:
```