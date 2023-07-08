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
	yum install -y php php-fpm php-cli php-curl php-mysqlnd php-mbstring php-devel </br>
 	systemctl restart httpd </br>
#Download code from this git repository and keep the code /var/www/html/
#Change db server address from config.php file 
  
# Create EC2 for Mariadb Server with Amazon Linux 2 
#Install Mariadb server on it. </br>
	yum install mariadb-server -y </br>
 	systemctl start mariadb </br>
  	systemctl status mariadb </br>
   	systemctl enable mariadb </br>

#Set your mariadb root passowrd and user for your databases </br>
#Run the following command and go as per guide:     </br>
     mysql_secure_installation </br>
#Now login to database with root and run the following command </br>
	create database demo </br>
 	GRANT ALL PRIVILEGES ON demo.* TO 'admin'@'%%' identified by 'admin123'; </br>
   

#create file name demo.sql with the following sql content:
    CREATE TABLE employees ( </br>
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT, </br>
    name VARCHAR(100) NOT NULL, </br>
    address VARCHAR(255) NOT NULL, </br>
    salary INT(10) NOT NULL ); </br>
#Now import Mysql dump file that you created demo.sql  </br>
	mysql -u admin -p demo < dump.sql </br>

 #All set for databse. 

    
    
#After create 2 VM now download this git code to Web Ec2  </br>
