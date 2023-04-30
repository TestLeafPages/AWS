*Hands on -1*

Find the below given Steps to install Apache + PHP + CRM app code + RDS

Step 1: Create an IAM user or use Existing IAM account

Step 2: Launch EC2 'Amazon Linux 2 AMI' & Create a *RDS MySQL(5.7)* DB Instance. Note Database name, HostName, UserName, Password

Step 3: Run the below command to install Apache server

connect to Ec2 Linux sever, open command line and Run the below commands

	sudo -i
	yum update -y
	yum install -y httpd
	systemctl start httpd
	systemctl enable httpd

4. Run the below command to install PHP

	sudo amazon-linux-extras install php7.2
	yum install php-mbstring
	yum-config-manager --enable remi-php72
	yum install php-pecl-zip
	yum install php-gd

*Reboot EC2 Instance* -> select instance -> Instance state -> reboot

5. Go to config file by using following command: *nano /etc/httpd/conf/httpd.conf*

In config file find the *<Directory "/var/www/html">* and change *AllowOverride None* to *AllowOverride All*

6. Stop and start apache :
	- *systemctl stop httpd*
	- *systemctl start httpd*

7. Run Following command to download CRM code to html folder 

	cd /var/www/html
	wget "https://www.espocrm.com/downloads/EspoCRM-5.8.2.zip"
	unzip EspoCRM-5.8.2.zip
	chmod -R 777 EspoCRM-5.8.2

Finally, go the public ip  from your browser.  http://<your linux public ip>/<Your CRM folder>  eg: http://13.23.24.25/EspoCRM-5.8.2  you should see CRM installation page

8. Fill all mandatory files, Database(RDS details) config, Admin Login.  
9. Once installation is done. Login to your new CRM. URL: "http://<IPv4 public address>/EspoCRM-5.8.2" .....  eg: http://13.23.24.25/EspoCRM-5.8.2

CRM installation steps:  https://www.espocrm.com/documentation/administration/installation

Output: you should see CRM login page.
