# RDS-Backed-S3-Media-Uploader
media uploader using RDS &amp; S3

1.	Launch a EC2 instance in amazon linux <br> 
2.	Create RDS with connection of instance 
3.	Create ACL enabled S3 bucket and give permission of read and write to public 
4.	Create IAM role for S3 full access and give this role to instance 
5.	Launch instance in powershell and install three services nginx, php, mariadb and start all the services
6.	Inside the instance at default path (/usr/share/nginx/html) create two files registration.html & upload.php
7.	at the same path install sdk to install there are lots of commands 
sudo curl -sS https://getcomposer.org/installer | sudo php <br>
sudo mv composer.phar /usr/local/bin/composer <br>
sudo ln -s /usr/local/bin/composer /usr/bin/composer <br>
sudo composer require aws/aws-sdk-php <br>
8.	finally with the endpoint of RDS get into database and create database and table
9.	Hit the IP on browser fill the form

