#!/bin/bash

# Update and upgrade the system
sudo apt-get update && sudo apt-get upgrade -y

# Install Apache web server
sudo apt-get install apache2 -y

# Install PHP and its required modules
sudo apt-get install php libapache2-mod-php php-mysql php-curl php-gd php-xml php-mbstring -y

# Install MySQL server
sudo apt-get install mysql-server -y

# Secure the MySQL installation
sudo mysql_secure_installation

# Install Ajenti
wget http://repo.ajenti.org/debian/key -O- | sudo apt-key add -
echo "deb http://repo.ajenti.org/ng/debian main main ubuntu" | sudo tee -a /etc/apt/sources.list
sudo apt-get update
sudo apt-get install ajenti -y

# Install Samba
sudo apt-get install samba -y

# Restart the Samba service
sudo service smbd restart

# Restart Apache web server
sudo service apache2 restart
