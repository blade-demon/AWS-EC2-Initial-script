# AWS-EC2-Boot-Script

####
  AWS-EC2 Web服务器启动脚本，安装nodejs,mongodb,nginx,

####
 
```sh
#!/bin/bash 
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
echo "deb [ arch=amd64,arm64 ] http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt-get update
sudo apt-get install -y nginx mongodb-org nodejs
sudo service mongod start
sudo service nginx start
sudo npm install -g bower
```
