# Student Registration Form(Dynamic Website-LEMP Stack)
## Intruduction
This is my first dynamic website, called Student Registration Form.
In this project, I deployed a dynamic web application using the LEMP stack (Linux, NGINX, MySQL, PHP) on an Amazon Linux EC2 server. The application allows users to fill out a registration form, and the submitted data is stored in a database.
The project helped me understand how frontend, backend, and database work together in a real-world environment.
## Architechture Diagram
![alt text](<imgs/architect 2.jpeg>)
## Technologies Used
* Amazon Linux (EC2)
* NGINX Web Server
* PHP->Backend
* MySQL Database
* HTML, CSS
* Linux Commands
## Features
* User registration form
* Data stored in database
* Dynamic data handling using PHP
* Server-side processing
* Accessible through server IP
## Steps I Followed
### 1. Launch Amazon Linux Instance<br>
* Created EC2 instance<br>
![alt text](<imgs/create a ec2 instance.png>)
* Connected using SSH
![alt text](<imgs/connect usin ssh.png>)

## 2.Install LEMP Stack
sudo yum update -y<br>
sudo yum install nginx php php-fpm<br> 
php-mysqlnd mariadb-server -y<br>
![alt text](<imgs/instaling packages.png>)

## 3.Start Services
sudo systemctl start nginx<br>
sudo systemctl enable nginx<br>

sudo systemctl start php-fpm<br>
sudo systemctl enable php-fpm<br>

sudo systemctl start mariadb<br>
sudo systemctl enable mariadb<br>
![alt text](<imgs/start services.png>)
## 4.Setup Database
* Login To MySQL:<br>
mysql -u root -p <br>

* Create database:<br>
CREATE DATABASE FCT;<br>

* Create table:<br>
USE FCT;<br>

CREATE TABLE students (<br>
    id INT AUTO_INCREMENT PRIMARY KEY,<br>
    name VARCHAR(100),<br>
    email VARCHAR(100)<br>
);<br>
![alt text](<imgs/create database.png>)

## 5.Create Project Files
* signup.html->for UI
* submit.php->for backend
![alt text](<imgs/create project files.png>)

## 6.Download connector
sudo yum install php8.5-mysqlnd.x86_64 -y<br>
![alt text](<imgs/download connector.png>)

## 7.Access Website
* open browser
* Enter EC@ public IP
* Fill The Form->Data stored in database
![alt text](<imgs/signup.html access.png>)

![alt text](<imgs/signup.html 2access.png>)

![alt text](<imgs/database fct.png>)
## 8.Database Details
* Database Name : FCT
* stores:<br>
     * name
     * email
     * website
     * comment
     * gender
## 9.What I Learned
* LEMP stack working
* PHP & MySQL integration
* Dynamic website deployment
* Handling user input
* Server configuration

## 10.Summary
This project helped me understand how dynamic websites work using the LEMP stack. I learned how data flows from user input to backend processing and gets stored in a database.
This is an important step in my journey towards full-stack development, DevOps, and cloud computing.