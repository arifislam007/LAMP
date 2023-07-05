# LAMP on Amazon Linux 

# This is a simple LAMP Stack for understandin application on aws with ec2 </br>

#Create EC2 Instance one for apache, php and another for mysql. Or you can do all thin in the same ec2. You should choose Amazon Linux 2 for Mysql servcie. </br>
#Now Follow the process: </br>
#Install apache: </br>
 	yum install -y httpd </br> </br>
  	systemctl start httpd </br>
   	systemctl enable httpd </br>
	
#Install PHP: </br>
	wget https://rpms.remirepo.net/enterprise/remi-release-7.rpm </br>
	yum install -y php php-fpm php-cli php-curl php-mysqlnd php-zip php-mbstring php-devel </br>
 	systemctl restart httpd </br>

#After create 2 VM now download this git code to Web Ec2  </br>
