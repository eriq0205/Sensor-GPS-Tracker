Third Rail Thickness Inspection Dashboard
📌 Overview

This dashboard is designed for our Final Year Project: Third Rail Thickness Inspection System.
It features:

1. Data localisation
2. Live camera visual via Flask webcam streaming
3. MySQL database integration for sensor data storage and retrieval
4. Apache web server hosting for dashboard access

⚙️ System Requirements

1. Ubuntu / Debian-based OS
2. Python 3.8+
3. Apache2
4. MySQL Server
5. PHP 7+
6. Git

Install Required Packages code:
sudo apt update && sudo apt upgrade -y
sudo apt install apache2 mysql-server php php-mysql libapache2-mod-php -y
sudo apt install python3 python3-pip python3-venv -y


Install Python Dependencies code:
pip3 install flask flask-cors opencv-python

*Steps to Configure MySQL Database*
1. Login to MySQL:
    - sudo mysql
      
2. Create database & user:
   - CREATE DATABASE sensor_data;
CREATE USER 'sensor_user'@'localhost' IDENTIFIED BY 'password123';
GRANT ALL PRIVILEGES ON sensor_data.* TO 'sensor_user'@'localhost';
FLUSH PRIVILEGES;
EXIT;

3. Import your existing database structure if available:
   - mysql -u root -p TrackEye01 
  
*Steps to Configure Apache*
1. Enable PHP and restart Apache:
   - sudo a2enmod php7.4
     sudo systemctl restart apache2

2. Ensure your dashboard PHP files are inside:
   - /var/www/html/sensor-tracker

*Steps to setup Flask Webcam Server*
1. Your webcam server script:
   -/var/www/html/sensor-tracker/webcam_server.py

*How to Auto-Run Services on Boot*
1. Apache & MySQL (These usually auto-start by default. If not) :
   -sudo systemctl enable apache2
    sudo systemctl enable mysql




