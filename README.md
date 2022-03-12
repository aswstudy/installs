
#!/bin/bash
# use this for your user data
# install httpd (linux 2 version)
sudo su
yum update -y
yum install -y httpd
systemctl start httpd.service
systemctl enable httpd.service
echo "hello world from $(hostname -f)" > /var/www/html/index.html
