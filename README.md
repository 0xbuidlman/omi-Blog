omi-blog
==========

omi's blog use beego framework

thanks ulricqin

##  environment 

```
sudo yum install go  
sudo yum install git  
sudo yum install mariadb-server mariadb  
sudo systemctl start mariadb.service  
mkdir ~/go
export GOPATH=~/go
go get github.com/beego/bee
``` 
environment variable
  
``` 
sudo vi /etc/profile
```  

export GOBIN=~/go/bin  
export GOPATH=~/go  
export PATH=$PATH:$GOBIN:$GOPATH  


## install

```
mkdir -p $GOPATH/src/github.com/darknessomi
cd $GOPATH/src/github.com/darknessomi
git clone https://github.com/darknessomi/omi-blog.git
go get github.com/darknessomi/omi-blog/...
cd omi-blog && modify conf/app.conf
setsid bee run
```
## mysql

```
create database omi_blog;
use omi_blog;
source ~/go/src/github.com/darknessomi/omi-blog/db.sql;
```


## admin 

```
url: /me
username: omi
password: md5
```
