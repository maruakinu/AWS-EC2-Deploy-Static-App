AWS EC2 Deployment of Static Application in Ubuntu
--------------------------------------------------

Project Overview
-----------------
The cloud is perfect for hosting static websites that only include HTML, CSS, and JavaScript files that require no server-side processing. In this project, deployed a static website to AWS using EC2 instance. 

1. Create and Launche an EC2 Instance with Ubuntu OS.
   <img width="1179" alt="Screenshot 2023-06-21 at 9 28 48 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/da8b8e39-a614-40ba-bcf1-9029860b3fa0">
   

2. Check the box in the right side of your instance and connect to it.
  <img width="1179" alt="Screenshot 2023-06-21 at 9 38 50 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/1d92ce3a-060d-4e2a-a029-2eb797a64850">

  <img width="804" alt="Screenshot 2023-06-21 at 9 41 33 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/db8759a5-634d-489c-9105-96762fb0540a">


3. Changing to root user and update latest packages on the system

        sudo su -
        sudo apt update

5. Installing Apache Web Server, checking the status of apache web server and Start the apache
   
        sudo apt install apache2 -y
        sudo systemctl status apache2
        sudo systemctl start apache2

6. Enable Apache to automatically start if the system restarted

       sudo systemctl enable apache2

7. Create directory, move to that directory and use wget to download files

       mkdir temp
       cd temp
       wget https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/archive/refs/heads/main.zip

8. Install unzip, unzip the file and Go to the directory of the file

       sudo apt-get install unzip
       unzip main.zip
       cd main

9. Move the file to /var/www/html

        mv * /var/www/html
 
10. Go to the Security part of your instance and click the security group link and click edit Inbound rules
    
     <img width="1166" alt="Screenshot 2023-06-21 at 10 05 31 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/1271e4f3-2e58-4a15-be10-3068b114e90d">

11. Add the additional inbound to your instances
    
   <img width="1265" alt="Screenshot 2023-06-21 at 10 08 18 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/daab0466-dac4-47c8-9d2b-50060a6106e2">


12. Type the public ip address of your instance to the browser
        
       
        
