Deploy application in monolithic and microservices architecture.

1).Deploying WordPress and MySQL in a Monolithic Architecture on AWS:-

*) Go to AWS cloud Services & Create EC2 instance.The Requirements for Ec2 instance are:-
*) Give a Name “ “
*) Use Ubuntu AMI (Ubuntu server 24.04 Lts SSD volume Type (free tire eligible)
*) select Instance Type t2. micro (Free tire eligible)
*) key Pair use your own or create one key-pair here i have used (jenkins-server)
*) network settings:- Edit here vpc i have used default, and subnet No preference and Enable Auto-assign public IP Network configuration Add Security group rule:- Type SSH, source type Anywhere ,Type Http, Anywhere, Mysql/Aurora
And Connect Through SSH I have Used Putty to connect




Here I have Installed a Mysql Server, Apache2, php and configure all in the single Ec2 instance I have Explained in Next Microservice Architecture There we will connect by common same Vpc Here there will be not there Remaining all same
2).Microservices Architecture on AWS: Deploying WordPress and MySQL on Separate EC2 Instances:-
Requirements:- Same as Above Ec2 Instances Here Create Two Ec2 Instances:-
*) For Mysql (Here sss,Mysql/Aurora same as above)
*) Wordpress(Here ssh, http, https, Mysql/Aurora) connect this Through Putty SSH one by one Both
*)And install And configure the Mysql And Create DataBase Name , UserName, Password, And Do FLUSH PRIVILEGES and Exit Mysql Server and Assign Security Configuration for this And Assign The Permissions For (RWE).. Here Configure Mysql to allow external connections like sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf here Change the Ip Address of example Bind-address =127.0.0.34 to 0.0.0.0 to allow connection from other services
*)For Wordpress Instance Insatll and configure Apache2, Php for wordpress and here configure Wodpress To connect To the database: like wp-config.php here you can use Nano Editor/Vim/vi.. i have used nano editor and change the Same What you have created in Mysql Server Datbase_Name, DB_user, DB_Password, DB_Host, And Ctrl+O to save and Confirm the Name for your File and exit (Ctrl+x)
*)After Insatlling apache2, Do Sudo systemctl enable apache2 sudo systemctl restart apache2
For secure The mysql and root password confirming Use sudo mysql_secure_installation
Finally go To ec2 instance of Wordpress And copy Ip address and paste to Any browser It will open WordPress if any errors troubleshoot by database connection Check the DB_name, user, password, and host as private address for Microservices and for Monolithic use localhost later do login and create own homepage and save and open in browser

