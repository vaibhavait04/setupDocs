# CONFIGURING APACHE CGI 

Add the config files .load to apache config load directory 
LoadModule cgi_module modules/mod_cgi.so

sudo cp /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/

Add the following lines to the /etc/apache2/sites-available/default-ssl.conf

       ServerName vaibhav-VirtualBox

       ScriptAlias /cgi-bin/ /usr/lib/cgi-bin/
       <Directory /usr/lib/cgi-bin>
	       AllowOverride None
	       Options +ExecCGI -MultiViews +SymLinksIfOwnerMatch
	       Order allow,deny
	       Allow from all
       </Directory>

Add the port mapping for the host to be available from virtual box. 
	127.0.0.1:81 for 10.0.2.15:80 

