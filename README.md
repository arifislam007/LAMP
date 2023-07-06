# LAMP on Amazon Linux 

# This is a simple LAMP Stack for understandin application on aws with ec2 </br>

#Create EC2 Instance one for apache, php and another for mysql. Or you can do all thin in the same ec2. You should choose Amazon Linux 2 for Mysql servcie. For apache you can chose AL 2023. </br>
#Now Follow the process: </br>
# Create a EC2 for apache with Amazon linux 2023.
#Install apache: </br>
 	yum install -y httpd </br> </br>
  	systemctl start httpd </br>
   	systemctl enable httpd </br>
	
#Install PHP: </br>
	yum install -y php php-fpm php-cli php-curl php-mysqlnd php-zip php-mbstring php-devel </br>
 	systemctl restart httpd </br>
  
# Create EC2 for Mariadb Server with Amazon Linux 2 
#Install Mariadb server on it. </br>
	yum install mariadb-server -y </br>
 	systemctl start mariadb </br>
  	systemctl status mariadb </br>
   	systemctl enable mariadb </br>
    
#After create 2 VM now download this git code to Web Ec2  </br>
