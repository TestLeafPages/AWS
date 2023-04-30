RDS, EC2  - Assignment

1. Create a **RDS MySQL(5.7.*) DB Instance**. Note the Database name, HostName(Endpoint), UserName, Password.
2. Launch a  EC2 Windows instance
 ```
	- Launch Windows Server 2022 Base  [Free Tier]
	- Choose Instance Type as t2.micro, skip 3 & 4 go to 5.  if required add tags
	- Configure Security Group to allow ports no (RDP 3389, HTTP-80) and set Source to anywhere 
	- Create a new KeyPair for windows  and download it
	- Confirm the windows  is up and running in Dashboard
```
Get windows server password from -> connect -> RDP client -> get Password

3. Connect Server using RDP
4. Download and install Xampp server(apache+php package) from below url
```
	Download Xampp: https://altushost-swe.dl.sourceforge.net/project/xampp/XAMPP%20Windows/7.2.28/xampp-portable-windows-x64-7.2.28-0-VC15-installer.exe
	installation steps:  https://www.wikihow.com/Install-XAMPP-for-Windows
	Start apache in xampp.
```
5. After installation open Xampp Control Panel and start the Apache server. 
6. Go to windows defender firewall with advanced settings, in inbound rule allow port 80.
7. Open browser in local system
8. Navigate to "http://<IPv4 public address>"  - you should see xampp welcome dashboard
9. go to instance and Download CRM app code from below given URL.

	https://wordpress.org/wordpress-5.8.zip

*to unzip use tool : https://www.7-zip.org/*

10. Unzip(7zip) the downloaded app code and move to following path : **"C:\xampp\htdocs" - eg: "C:\xampp\htdocs\<YOUR APP CODE FOLDER NAME>"**
11. Open browser in local system  Navigate to http://<IPv4 public address>/<YOUR APP CODE FOLDER NAME> - you should see Wordpress installation page
12. Full the mandatory files such as, Admin Logins, Database config.
13. Wait for few minutes to complete installation. 
14. Once installation is done. open URL: http://<IPv4 public address>/<YOUR APP CODE FOLDER NAME>. 
