
#apt update -y
#adduser todoapp
#su - todoapp
$git clone https://github.com/zelar-soft-todoapp/users.git
 
$sudo apt install openjdk-8-jdk
$sudo apt install maven
$sudo mvn package

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

#sytemctl daemon-reload
#systemctl restart user
#systemctl status user














































![image](https://user-images.githubusercontent.com/82602260/116801312-446c7e80-ab26-11eb-9fc8-81a8a6ff09ef.png)
