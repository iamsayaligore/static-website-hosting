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
   ![alt text](<lunch instance.png>)

2. Choose Amazon Linux 2 (free tier).
3. ![alt text](linux.png)

4. Select t3.micro (Free tier eligible).

5. Configure:
Security Group → allow HTTP (port 80) and SSH (port 22).

1. Launch the instance 
  ![alt text](instance.png) 
   
**Step 2: Connect to EC2 Instance**

Open terminal and connect:

ssh -i "private key.pem" ec2-user@ec2-public-IP

![alt text](connect.png)

**Step 3: update system and Install Apache webserver**
 
       sudo yum update -y

       sudo yum install httpd -y
   
 ![alt text](image.png)
**Step 4: Start,enable and status the apache server**

        sudo systemctl start httpd 

       sudo systemctl enable httpd

       sudo system status httpd

   ![alt text](image-1.png)

**Step 5: Setup website Directory**

1.Created a project folder under 
   
        cd/var/www/html
2.Create an index.html

        sudo vim index.html

   ![alt text](image-2.png)

3Add the following content:

      <h1>This is my first webserver</h1>

![alt text](image-3.png) 

**Step 5: check result**

1 open your Browser and enter your public IP address 

![alt text](image-4.png)





   
