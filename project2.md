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
















