# EC2 Nginx Deployment
## Overview
In this project I launched an EC2 instance and deployed a simple Nginx web server.
## Steps Performed
1. Created an EC2 instance
2. Connected using SSH
3. Installed Nginx
4. Started the web server
5. configured Security groups
### Commands used
- cretaed an EC2 instance and connected to it via EC2 instance connect and went ahead to install the web server software
https://github.com/Raissa-94/AWS-Learning/blob/main/Week1/Screenshot%20(266).png?raw=true 
### Install Nginx
sudo yum install nginx -y
### Start Nginx
sudo systemctl start nginx
### Enable Nginx
sudo systemctl enable Nginx
### System Status
this is to know if the system is active and running
sudo systemctl status nginx 
### Check to seee if the default nginix message like welcome to Nginix will be displayed
- The first time i did it did not work out because there was no inbound traffic rule allowing traffic on port 80 since nginx work by default on port 80, so i edited the inbound security rule by allowing HTTP traffic on port 80 from all IP addresses and when i reloaded the page the **welcome to Nginx** messaged was displayed.
https://github.com/Raissa-94/AWS-Learning/blob/main/Week1/Screenshot%20(265).png?raw=true
- The EC2 Instance connect terminal displays the content of the nginix file, Nginx.conf.
- I edited the nginx file to display my own custom content **Welcome to Raissa's Eazy Life Restaurant** by continuing with the following commands
### Edit file
nano /etc/nginx/nginx.conf
### To Change the Nginx content to my custom content
cd /usr/share/nginx/html/
### To delete the content of the nginx file
* nano index.html
* sudo rm indext.htlm
- Added my custom index.html file to display the home page of my website with header " Welcome to Raissa's Eazy Life Restaurant" 
**sudo nano index.html**
