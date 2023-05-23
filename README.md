# ubuntu-22.04
#### Install Apache 2 ( https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-22-04#step-2-adjusting-the-firewall )
- sudo apt update
- sudo apt install apache2

#### Firewall setup
- sudo ufw app list
- sudo ufw allow 'Apache Full'
- sudo systemctl status apache2
#### Install Certbot for auto SSL ( https://www.digitalocean.com/community/tutorials/how-to-use-certbot-standalone-mode-to-retrieve-let-s-encrypt-ssl-certificates-on-ubuntu-22-04 )
- sudo snap install core; sudo snap refresh core
- sudo apt remove certbot
- sudo snap install --classic certbot
- sudo ln -s /snap/bin/certbot /usr/bin/certbot
- sudo certbot certonly --standalone -d your_domain -d your_other_domain
#### Install MySQL
- apt update
- apt install mysql-server

#### Install PHP 8.1 ( https://www.digitalocean.com/community/tutorials/how-to-install-php-8-1-and-set-up-a-local-development-environment-on-ubuntu-22-04 )
- sudo apt install --no-install-recommends php8.1
