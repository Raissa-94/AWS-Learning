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
- cretaed an EC2 instance and connected to it via EC2 instance connect and went ahead to install the web server software. the first time i tried connecting it didnt work because there was no inbound rule allowing trafic on port 22.
  ![Security Group SSH Rule](Screenshot%20(267).png)

Then i added new rule for SSH allowing trafic on port 22 from anywhere 0.0.0.0/0
![Security Group SSH Rule](Screenshot%20(266).png)

### Install Nginx
sudo yum install nginx -y
### Start Nginx
sudo systemctl start nginx
### Enable Nginx
sudo systemctl enable Nginx
### System Status
this is to know if the system is active and running
sudo systemctl status nginx 

![System status](Screenshot%20(268).png)

### Check to seee if the default nginix message like welcome to Nginix will be displayed
- The first time i did it did not work out because there was no inbound traffic rule allowing traffic on port 80 since nginx work by default on port 80, so i edited the inbound security rule by allowing HTTP traffic on port 80 from all IP addresses and when i reloaded the page the **welcome to Nginx** messaged was displayed.

![Security Group SSH Rule](Screenshot%20(265).png)

- The EC2 Instance connect terminal displays the content of the nginix file, Nginx.conf.

![Security Group SSH Rule](Screenshot%20(270).png)

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

![Security Group SSH Rule](Screenshot%20(271).png)

![Security Group SSH Rule](Screenshot%20(272).png)

