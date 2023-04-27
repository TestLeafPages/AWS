Hi Team, 

EC2 Linux Assignment - login as IAM user check you have following policies (AdminisratorAccess)

Choose your regions - eg. mumbai, singapore

1. Launch *Amazon Linux 2 AMI (HVM)*, SSD Volume Type [Free Tier]
2. Choose Instance Type as t2.micro, skip 3 instance configuration & go to 4.
3. Configure Storage with 8 GB 
4. Configure Security Group to allow ports no (SSH-22, HTTP-80) and set Source to anywhere 
5. Create a new KeyPair for Linux and download it
6. Confirm the Linux is up and running in Dashboard

Process to connect Ec2 instance

1. open command line from the downloaded Linux key pair (.pem)
 	type the following command 

   Syntax: ssh -i "path of pem file/pemfile.pem" ec2-user@public-ip

   EG: ssh -i linux.pem ec2-user@13.121.346.124

Run following commands one by one to install apache 

sudo -i
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
cd /var/www/html
touch index.html
nano index.html

use this code in index.html file
--------------------

<!DOCTYPE html>
<html>
<body>

<h1>Hello World</h1>
<h2>This is my 1st ec2 linux instance</h2>


</body>
</html>

-----------------


to save index file : CTRL + X
			Y
			Enter->

Finally, go the public ip from your chrome

http://<your linux public ip>

That confirms you apache httpd is up and running in Linux