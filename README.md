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
- Success log looks like this
- Saving debug log to /var/log/letsencrypt/letsencrypt.log
- Requesting a certificate for your_domain and your_other_domain

- Successfully received certificate.
- Certificate is saved at: /etc/letsencrypt/live/domain.com/fullchain.pem
- Key is saved at:         /etc/letsencrypt/live/domain.com/privkey.pem
- This certificate expires on 2023-08-20.
- These files will be updated when the certificate renews.
- Certbot has set up a scheduled task to automatically renew this certificate in the background. 
