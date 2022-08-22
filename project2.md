## Step1 

## INSTALLING THE NGINX WEB SERVER

`sudo apt update`

![apt update](./images/apt-update.PNG)


`sudo apt install nginx`

![Install nginx](./images/nginx-install.PNG)


`sudo systemctl status nginx`

![nginx status](./images/ngnix-status.PNG)


`curl http://127.0.0.1:80`

![curl nginx ](./images/curl-confirm.PNG)


`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`

![server ip ](./images/server-ip.PNG)


`http://<Public-IP-Address>:80`

![nginx page ](./images/nginx-page.PNG)


## Step2

## INSTALLING MYSQL

`sudo apt install mysql-server`

![apt update](./images/sql-install.PNG)

`sudo mysql -p`
![Sql login](./images/sql-login.PNG)


`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`
![Sql password change](./images/password-sql.PNG)

`exit`
![Sql exit](./images/exit-sql.PNG)

`sudo mysql_secure_installation`
![Sql exit](./images/secure-sql.PNG)

`sudo mysql -p`
![sudo mySql ](./images/sql-p.PNG)

`exit`
![mySql exit ](./images/exit.PNG)


## Step3

## INSTALLING PHP

`sudo apt install php-fpm php-mysql`
![php install ](./images/php-install.PNG)


## Step4

##  CONFIGURING NGINX TO USE PHP PROCESSOR

`sudo mkdir /var/www/projectLEMP`
![mkdir projectlemp ](./images/projectlamp.PNG)

`sudo chown -R $USER:$USER /var/www/projectLEMP`
![mkdir projectlemp ](./images/chown-projectlemp.PNG)

`sudo nano /etc/nginx/sites-available/projectLEMP`
![vi projectlemp ](./images/vi-projectlemp.PNG)

`sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/`
![vi activating nginx ](./images/projectcon.PNG)

`sudo unlink /etc/nginx/sites-enabled/default`
![vi relaod nginx ](./images/reload-nginx.PNG)

` sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html`

![lemp index ](./images/lemp-index.PNG)

## Step5

##  TESTING PHP WITH NGINX

`sudo nano /var/www/projectLEMP/info.php`
![Nano info.php ](./images/nano-info.PNG)

`http://`server_domain_or_IP`/info.php`
![info page ](./images/info-page.PNG)

## Step6

##  RETRIEVING DATA FROM MYSQL DATABASE WITH PHP

`sudo mysql`
![info page ](./images/sql-log.PNG)

`mysql> CREATE DATABASE `example_database`;`
![example database ](./images/example-db.PNG)

`mysql>  CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';`
![example database user](./images/example-user.PNG)


`GRANT ALL ON example_database.* TO 'example_user'@'%';`
![Grant permission](./images/permission.PNG)

`exit`

![Grant permission](./images/exit-db.PNG)

`mysql -u example_user -p`
![example user](./images/example-sql.PNG)

`mysql> SHOW DATABASES;`
![example user](./images/database-show.PNG)


`create todo list`
![example user](./images/todo.PNG)

`INSERT INTO example_database.todo_list (content) VALUES ("My first important item");`

![insert todo](./images/insert-todo.PNG)

`SELECT * FROM example_database.todo_list;`

![insert todo](./images/view-todo.PNG)

` exit`
![exit todo](./images/exit-sql.PNG)

`nano /var/www/projectLEMP/todo_list.php`
![exit todo](./images/nano-todo.PNG)

`http://<Public_domain_or_IP>/todo_list.php`
![exit todo](./images/php-web.PNG)






































