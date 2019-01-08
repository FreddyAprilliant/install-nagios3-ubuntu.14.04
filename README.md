# Install nagios3 on ubuntu.14.04
Step by step install nagios3 on ubuntu 14.04 (trusty) it's better to run all command in super user mode (su) or if you wish you could use "sudo" instead.

## Install and start Apache Server
1. Install apache2 :
	
	`~#apt-get -y install apache2`
    
2. Configure apache2, change line below :
    
		`~#vi /etc/apache2/conf-enabled/security.conf`
        
		_#line 26: change_
		`ServerTokens Prod`
      
			  _#line 37: change_
       `ServerSignature Off`
        
  `~#vi /etc/apache2/mods-enabled/dir.conf`
        _#line 2: add file name that it can access only with directory's name_
        DirectoryIndex index.html index.htm
        
  `~#vi /etc/apache2/apache2.conf`
        _#line 70: add server name_
        ServerName www.mynagios.com
    
  ~#vi /etc/apache2/sites-enabled/000-default.conf
        *#line 11: change admin email address (you don't have to change it if you run it locally)
        ServerAdmin webmaster@gmail.com
        
  ~#/etc/init.d/apache2 restart
        *restart web server apache2

3. 
