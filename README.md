adding user and cloning repo
```
#apt update -y
need to create an user 
#adduser todoapp
#su - todoapp
$git clone https://github.com/zelar-soft-todoapp/users.git
 ```
 
 installation of java and maven
 ```
$sudo apt install openjdk-8-jdk
$sudo apt install maven
$sudo mvn package
```
after this jar files will be created in target folder

so , this path has to give in service file 
```
#vi user.service

[Unit]
Description=user Service
[Service]
User=todoapp
Environment=SERVER_PORT=8080
Environment=JWT_SECRET=foo
ExecStart=/bin/java -jar /home/todoapp/user.jar
SyslogIdentifier=user
[Install]
WantedBy=multi-user.target
```
after this need to start the user service 
```
#sytemctl daemon-reload
#systemctl restart user
#systemctl status user
```







![image](https://user-images.githubusercontent.com/82602260/116801312-446c7e80-ab26-11eb-9fc8-81a8a6ff09ef.png)


![Screenshot (261)](https://user-images.githubusercontent.com/82602260/116852696-693e2000-ac12-11eb-9e91-bf836a857998.png)

