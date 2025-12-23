history
sudo dnf groupinstall "Development Tools"
mkdir ~/sandbox
cd ~/sandbox
wget https://dlcdn.apache.org/httpd/httpd-2.4.66.tar.gz
tar xvfz httpd-2.4.66.tar.gz
wget https://dlcdn.apache.org//apr/apr-1.7.6.tar.gz
wget https://dlcdn.apache.org//apr/apr-util-1.6.3.tar.gz
tar xvfz apr-1.7.6.tar.gz
tar xvf apr-util-1.6.3.tar.gz
mv apr-1.7.6 httpd-2.4.66/srclib/apr
mv apr-util-1.6.3 httpd-2.4.66/srclib/apr-util
sudo dnf install pcre-devel
sudo dnf install -y expat-devel
./configure --prefix=/home/ec2-user/dev/apache
make
make install
cd /home/ec2-user/dev/apache
sudo bin/apachectl start
cd ~/dev/apache/
ls -altr
sudo bin/apachectl start
sudo lsof -i :80
curl localhost
##  java
curl -s "https://get.sdkman.io" | bash
. ~/.bash_profile
sdk list java
sdk install java 21.0.9-amzn
cd ~/dev
curl -O https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.50/bin/apache-tomcat-10.1.50.tar.gz
tar xvfz apache-tomcat-10.1.50.tar.gz
cd apache-tomcat-10.1.50/
bin/startup.sh
lsof -i :8080
curl localhost:8080
cd ~/dev/apache
cd conf/
ls -altr
vi httpd.conf
cd ../bin
ls -atrl
history | grep apache
sudo ./apachectl -t
sudo ./apachectl restart
curl localhost/app
cd ~/dev/apache-tomcat-10.1.50/webapps/
cd ROOT
mkdir app
cd app
vi index.jsp
cd ../..
cd examples/
jar cvf ../app.war *
mv app.war app.war_
