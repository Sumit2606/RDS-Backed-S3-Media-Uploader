# RDS-Backed-S3-Media-Uploader
media uploader using RDS &amp; S3

1.	Launch a EC2 instance in amazon linux <br> 
2.	Create RDS with connection of instance 
3.	Create ACL enabled S3 bucket and give permission of read and write to public 
4.	Create IAM role as S3 full access and give this role to EC2 instance 
5.	Launch instance in powershell and install three services nginx, php, mariadb and start all the services
   sudo yum install nginx php maraidb105-server -y
   sudo service nginx start
	 sudo service php-fpm start
6.	Inside the instance at default path (/usr/share/nginx/html) create two files registration.html & upload.php
   cd /usr/share/nginx/html/
   sudo nano registration.html
   sudo nano upload.php
7.	at the same path install sdk, the commands are <br>
sudo curl -sS https://getcomposer.org/installer | sudo php <br>
sudo mv composer.phar /usr/local/bin/composer <br>
sudo ln -s /usr/local/bin/composer /usr/bin/composer <br>
sudo composer require aws/aws-sdk-php <br>
8. finally with the endpoint of RDS get into database and create database and table
   sudo mysql -u admin -p -h RDS_Endpoint
   create database facebook;
   use facebook;
   create table users(id int primary key,name varchar(50),surname varchar(50),gender varchar(50),email varchar(50),image_url varchar(50));
13.	Hit the IP on browser & fill the form

