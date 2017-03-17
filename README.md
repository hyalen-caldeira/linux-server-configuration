# linux-server-configuration
Linux (Ubuntu) configuration using _Virtual Box, Vagrant, AWS Lightsail, AWS EC2 and many others ..._

Although there isn't too much to see, in this _example project_ I could:
- Configure a virtual machine
- Configure the Uncomplicated Firewall (UFW) to only allow access to some ports (including SSH)
- Configure the SSH access
- Forward the host ports to be accessed by guest ones
- Manage user access
- Install some apps like PostgreSQL, Git and Apache 

All these steps were done **local**, in the **AWS Lightsail** and **AWS EC2** 

Once installed the Apache, procede with the following basic configurations:
- In order to prevent the Apache Web Server from displaying operation system errors, add the following two lines in /etc/apache2/apache2.conf file. The “ServerTokens Prod” option tells the web server to return only apache and suppress the OS major and minor version. After modifying the configuration file, you have to restart/reload your apache web server to make it effective.
  - ServerSignature Off
  - ServerTokens Prod
- By default your apache web server will show all the content of the document root directory if it does not have an index file. This feature can be turn off for a specific directory through “options directive” available in the Apache configuration file.
  - Directory /var/www/html Options -Indexes /Directory

_This README is just a very simple initial version. The idea is to let documented all was done._
