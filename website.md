# Static Website Deployment on AWS EC2 using Apache Webserver

## **Objective**
To host and deploy a static website (HTML)on an AWS Amazon linux EC2 Instance using apache http server (httpd).

## **Prerequisites**
1. AWS Account 
2. A key pair (.pem file) SSH Client
3. Basic Knowledge of linux commands  
4. A static website (Html)ready
   

## **Steps**
**step 1: Launch an EC2 Instance**

1. Go to AWS Management Console → EC2 → Launch Instance.
   ![alt text](<WhatsApp Image 2025-11-12 at 18.41.29_feba0bc8.jpg>)

2. Choose Amazon Linux 2 (free tier).
3. ![alt text](<WhatsApp Image 2025-11-12 at 18.41.30_1924cf78.jpg>)

4. Select t3.micro (Free tier eligible).

5. Configure:
Security Group → allow HTTP (port 80) and SSH (port 22).

1. Launch the instance 
  ![alt text](instance.png) 
   
**Step 2: Connect to EC2 Instance**

Open terminal and connect:

ssh -i "private key.pem" ec2-user@ec2-public-IP

![alt text](<WhatsApp Image 2025-11-12 at 18.41.31_29d924de.jpg>)

**Step 3: update system and Install Apache webserver**
 
       sudo yum update -y

       sudo yum install httpd -y
   
 ![alt text](<WhatsApp Image 2025-11-12 at 18.41.32_b1d8e9f0.jpg>)
**Step 4: Start,enable and status the apache server**

        sudo systemctl start httpd 

       sudo systemctl enable httpd

       sudo system status httpd

   ![alt text](<WhatsApp Image 2025-11-12 at 18.41.32_2f8a5b83.jpg>)

**Step 5: Setup website Directory**

1.Created a project folder under 
   
        cd/var/www/html
2.Create an index.html

        sudo vim index.html

  

3Add the following content:

      <h1>This is my first webserver</h1>

![alt text](<WhatsApp Image 2025-11-12 at 18.41.32_5db3d7f5.jpg>) 

**Step 5: check result**

1 open your Browser and enter your public IP address 

![alt text](<WhatsApp Image 2025-11-12 at 18.41.23_cb47cc7b.jpg>)





   
