AWS EC2 Deployment of Static Application in Ubuntu

1. Create and Launche an EC2 Instance with Ubuntu OS.
   <img width="1179" alt="Screenshot 2023-06-21 at 9 28 48 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/da8b8e39-a614-40ba-bcf1-9029860b3fa0">
   

2. Check the box in the right side of your instance and connect to it.
  <img width="1179" alt="Screenshot 2023-06-21 at 9 38 50 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/1d92ce3a-060d-4e2a-a029-2eb797a64850">

  <img width="804" alt="Screenshot 2023-06-21 at 9 41 33 PM" src="https://github.com/maruakinu/AWS-EC2-Deploy-Static-App/assets/100325935/db8759a5-634d-489c-9105-96762fb0540a">


3. Changing to root user and update latest packages on the system

        sudo su -
        sudo apt update

5. Installing Apache Web Server
   
        sudo apt install apache2 -y

6. Checking the status of apache web server and Start the apache

        sudo systemctl status apache2
        sudo systemctl start apache2

7. Enable Apache to automatically start if the system restarted

       sudo systemctl enable apache2

8. Create directory, move to that directory and use wget to download files

       mkdir temp
       cd temp
       wget https://www.free-css.com/assets/files/free-css-templates/download/page292/settle.zip

9. Install unzip, unzip the file and Go to the directory of the file

       sudo apt-get install unzip
       unzip settle.zip
       cd settle

11. Move the file to /var/www/html

        mv * /var/www/html
 
    
       
        
