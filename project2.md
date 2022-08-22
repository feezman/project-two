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








