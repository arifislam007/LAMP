# LAMP on Amazon Linux 

# This is a simple LAMP Stack for understandin application on aws with ec2

#Create EC2 Instance one for apache, php and another for mysql. Or you can do all thin in the same ec2. You should choose Amazon Linux 2 for Mysql servcie. 
Now Follow the process:
#Install apache:
 	yum install -y httpd
	
#Install PHP: 
	wget https://rpms.remirepo.net/enterprise/remi-release-7.rpm
	yum install -y php php-fpm php-cli php-curl php-mysqlnd php-zip php-mbstring php-devel

#After create 2 VM now download this git code to Web Ec2 
