# Install nagios3 on ubuntu.14.04
Step by step install nagios3 on ubuntu 14.04 (trusty) it's better to run all command in super user mode (su) or if you wish you could use "sudo" instead.

## Install and start Apache Server

1. Install apache2 : `#apt-get -y install apache2`
2. Open file _**security.conf**_ : `#vi /etc/apache2/conf-enabled/security.conf`
3. Change **line #26** `ServerTokens Prod` and **line #37** `ServerSignature Off`
4. Open file _**dir.conf**_ : `#vi /etc/apache2/mods-enabled/dir.conf`
5. Change **line #2** : _add file name that it can access only with directory's name_
   <br>`DirectoryIndex index.html index.htm`
6. Open **file apache2.conf** : `~#vi /etc/apache2/apache2.conf`
7. Change **line #70** : _add server name_
   <br>`ServerName www.mynagios.com`
8. Open file **000-default.conff** : `~#vi /etc/apache2/sites-enabled/000-default.conf`
9. Change **line #11** : _change admin email address (you don't have to change it if you run it locally)_
   <br>`ServerAdmin webmaster@gmail.com`
10. Restart apache2 web server : `#/etc/init.d/apache2 restart`

