 # How to Setup WordPress Website Using LAMP Stack

 Setting up a WordPress website using the LAMP stack (Linux, Apache, MySQL, PHP) is a powerful way to create a robust and scalable web presence. This project will guide you through each step of the process, from setting up your server environment to installing WordPress and configuring it for optimal performance. Whether you're a seasoned developer or a beginner, this tutorial will provide you with the knowledge and skills needed to deploy a fully functional WordPress site. By the end of this guide, you'll have a solid understanding of how to leverage the LAMP stack to build and manage your own WordPress website, ensuring a secure, efficient, and customizable platform for your content.

Key Features:

Step-by-step instructions for installing and configuring LAMP components.
Secure database creation for your WordPress website.
User-friendly guide for completing the WordPress installation process.

Benefits:
Gain independence by managing your own WordPress website.
Understand the core technologies behind WordPress.
Customize your website to your exact needs.
Embrace the flexibility and power of WordPress.

Introduction
Before we begin, let's review the tools we'll be using throughout this project.

Linux
Linux is the cornerstone of the LAMP stack, serving as the operating system that underpins the entire infrastructure. As an open-source and highly customizable platform, Linux provides a stable and secure environment for hosting web applications. Its efficiency in handling processes and resources makes it an ideal choice for web servers. In a LAMP stack, Linux coordinates the interaction between Apache (the web server), MySQL (the database), and PHP (the scripting language), ensuring seamless operation and communication between these components. This foundation allows for high performance, flexibility, and scalability, making Linux a crucial element in the successful deployment and management of a LAMP-based WordPress website.

Apache
Apache is a critical component of the LAMP stack, acting as the web server that handles client requests and serves web content. As an open-source and widely used web server software, Apache is known for its reliability, security, and flexibility. In a LAMP stack, Apache processes incoming HTTP requests, fetching and delivering web pages to users' browsers. It also supports various modules that extend its functionality, such as URL redirection, authentication, and load balancing. By efficiently managing web traffic and providing a stable platform for running web applications, Apache ensures that your WordPress website runs smoothly and can handle a large number of concurrent users.

MySQL
MySQL is the database management system within the LAMP stack, responsible for storing and managing the data that powers your web applications. As an open-source relational database, MySQL offers robust performance, scalability, and security. In the context of a LAMP stack, MySQL works closely with PHP to handle data operations such as storing user information, retrieving content, and managing transactions. For a WordPress website, MySQL stores all the content, user data, settings, and other essential information, allowing for dynamic content generation and efficient data retrieval. By ensuring data integrity and providing powerful querying capabilities, MySQL plays a crucial role in maintaining the functionality and performance of a WordPress site on the LAMP stack.

PHP
PHP is the scripting language in the LAMP stack, responsible for generating dynamic web content. As a server-side language, PHP processes code on the web server to create HTML content that is then sent to the user's browser. In the LAMP stack, PHP works in tandem with Apache to handle web requests and interact with the MySQL database to retrieve and manipulate data. For a WordPress website, PHP executes the core logic that powers the site, managing everything from user authentication to content management and plugin functionality. By seamlessly integrating with Apache and MySQL, PHP ensures that your WordPress site is dynamic, interactive, and capable of delivering a rich user experience.

Project 4
S/N	Project Tasks
1	Deploy an Ubuntu Server
2	Set up your LAMP stack on the server
3	Configure the wordpress Application
4	Map the IP address to the DNS A record
5	Validate the WordPress website setup by accessing the web address.

Key Concepts Covered
AWS (EC2 and Route 53)
Linux(Ubuntu)
Apache
MySQL
PHP
Wordpress
DNS
SSL (certbot)
OpenSSL command


Checklist
 Task 1: Deploy an Ubuntu Server
 Task 2: Set up your LAMP stack on the server
 Task 3: Configure the wordpress Application
 Task 4: Map the IP address to the DNS A record
 Task 5: Validate the WordPress website setup by accessing the web address.

# Documentation
Ubuntu server was spinned up taking reference from project 1

setting up inbound rule for MYSQL in the security group. Click on Security and select the Security group. 
![pic](img)


Click on Edit inbound rules to add rule
![pic](img)

I Clicked on Custom TCP to select MySQL/Aurora!
[pic](img)


IP address was added to allow access and restrict it to MySQL exclusively to the Web Server’s IP address. (inbound Rule configuration, specify the source as /32) then click Save rules
![pic](img)


Connected to your Ubuntu server via SSH using terminal

![pic](img)

# Instalation of Apache
To install Apache, the following commands was used in your terminal.

sudo apt update
sudo apt install apache2

![pic](img)
![pic](img)


To enable Apache to start on boot, execute sudo systemctl enable apache2, and then verify its status with the sudo systemctl status apache2 command.
![pic](img)


let's check if our server is running and accessible both locally and from the Internet by executing the following command: curl http://localhost:80.

![pic](img)




