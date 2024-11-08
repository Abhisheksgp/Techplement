# Techplement
Deploy application in monolithic and microservices architecture.
1).Deploying WordPress and MySQL in a Monolithic Architecture on AWS:-
Go to AWS cloud Services Create EC2 instance Requirements for Ec2 instance are:-
*) Give a Name “ “
*) Use Ubuntu AMI (Ubuntu server 24.04 Lts SSD volume Type (free tire eligible)
*) select Instance Type t2. micro (Free tire eligible)
*) key Pair use your own or create one key-pair here i have used (jenkins-server)
*) network settings:- Edit here vpc i have used default, and subnet No preference and Enable Auto-assign public IP Network configuration Add Security group rule:- Type SSH, source type Anywhere ,Type Http, Anywhere, Mysql/Aurora
And Connect Through SSH I have Used Putty to connect
