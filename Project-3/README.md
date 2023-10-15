# WEBSTACK IMPLEMENTATION (LEMP STACK) 

## Installing Nginx Server 

We'll use `sudo apt update` to update the server's package index and `sudo apt install nginx` to install the Nginx server.

![Alt text](<Images/Screenshot (261).png>)

![Alt text](<Images/Screenshot (262).png>)

To access the new server locally on Ubuntu shell we run `curl http://localhost:80` 

![Alt text](<Images/Screenshot (264).png>) 

To test the Nginx server's response to request from the internet, we'll type the IP address on a web browser. http://ip address:80 

![Alt text](<Images/Screenshot (272).png>) 

## Installing MySQL 

MySQL, a Relational Database Management System, is installed with `sudo apt install mysql-server`. 

![Alt text](<Images/Screenshot (273).png>) 

Set security script in the mysql console by typing: `ALTER USER 'root'@'localhost'IDENTIFIED WITH mysql_nativea-password BY 'PassWord.1';` 

![Alt text](<Images/Screenshot (284).png>) 

Start interactive script by running `sudo mysql_secure_installation`. 

You will be asked to configure the validate password plugin. You will be shown the password strenth for the root password you just entered. Enter Y if you are satistied and for the rest of the querry. 

![Alt text](<Images/Screenshot (276).png>) 

![Alt text](<Images/Screenshot (277).png>) 

## Installing PHP 

Install PHP using `sudo apt install php-fpm php_mysql`. 

![Alt text](<Images/Screenshot (284).png>) 

## Configuring Nginx to Use PHP Processor 

First, we'll create a directory structure within /var/www for the your_domain website using 
 `sudo mkdir /var/www/projectLEMP` 

Next, assign ownership of the directory with the $USER environment variable as follows 
 `sudo chown -R $USER:$USER /var/www/projectLEMP`  

Next, open a new configuration file in Nginx's `sites-available` directory using nano command line editor. 
 `sudo nano etc/nginx/sites-available/projectLEMP` 

It will create a new blank file and a bare-bone configuration will be put in it as follows. 

![Alt text](<Images/Screenshot (285).png>) 

Activate the configuration by linking to the config file from Nginx's `sites-enabled` directory: 
 `sudo ln -s /etc/nginx/sies-available/projectLEMP /etc/nginx/sites-enabled/` 

 Test the configuration for syntax error by typing: `sudo nginx -t` 

 Next, we'll disable default Nginx host currently configured to listen on port 80. 
  `sudo unlink /etc/nginx/sites-enabled/default` 

  Now we can reload nginx using `sudo systemctl reload nginx` 

  ![Alt text](<Images/Screenshot (287).png>) 

Now, we'll create an index.html file in our empty /var/www/projectLEMP web root to test that our new server block works as expected. 

![Alt text](<Images/Screenshot (289).png>) 

Now go to the browser to open the URL using the IP address. 

![Alt text](<Images/Screenshot (288).png>) 

## Testing PHP with Nginx 

To test if Nginx can corerectly hand `.php` files off to PHP Processor. 

Open a new file called `info.php` within the document root in the text editor. 

Type the following lines in the new file 
 
 `<?php
 
 phpinfo();` 

![Alt text](<Images/Screenshot (289).png>) 

Now we can access the server using the domain name or IP address as follows: 
`http://server_domain_or_IP/info.php` 

![Alt text](<Images/Screenshot (290).png>) 

## Retrieving Data From MySQL Database with PHP 

First, we'll create a test Database with simple "To do list" and configure access to it, so the Nginx website would be able to query data from the Database and display it. 

Use `sudo mysql -p` to log into the MySQL console. 

To create a new Database we'll run the following command: `mysql> CREATE DATABASE `example_database`;`

Now, we'll create a new user and grant full access on the newly created database as follows: 
 `mysql>  CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';` 

We'll grant the new user permission as follows: 
 `mysql> GRANT ALL ON example_database.* TO 'example_user'@'%';`

![Alt text](<Images/Screenshot (293).png>) 

We'll test if the new user has proper permissions by logging into the MySQL console again using the custom user credentials. 
We'll type: `mysql -u example_user -p` 

Confirm that you have access to the `example_database` database by typing `SHOW DATABASES;` in MySQL console. It will bring out some output. 

![Alt text](<Images/Screenshot (295).png>) 

Next, we'll create a table named todo_list as follows: 
 `CREATE TABLE example_database.todo_list (item_id INT AUTO_INCREMENT,content VARCHAR(255),PRIMARY KEY(item_id));` 

Insert a few rows of content in the test table repeatedly with different values as follows: 
 `INSERT INTO example_database.todo_list (content) VALUES ("My first important item");` 

![Alt text](<Images/Screenshot (296).png>) 

![Alt text](<Images/Screenshot (297).png>) 

To confirm that the Data was successfully stored, run: `SELECT * FROM example_database.todo_list;` 

![Alt text](<Images/Screenshot (298).png>) 

Now, we'll create a PHP script that will connect to MySQL in our custom web root directory as follows: 
 `nano /var/www/projectLEMP/todo_list.php` 

![Alt text](<Images/Screenshot (301).png>) 

![Alt text](<Images/Screenshot (300).png>) 

We can now access the page in our web browser as follows: `http://<Public_domain_or_IP>/todo_list.php` 

![Alt text](<Images/Screenshot (304).png>) 

CONCLUSION 

We have built a flexible foundation for serving PHP websites and applications to our visitors, using Nginx as web server and MySQL as database management system. 

Thank you and God bless you. 