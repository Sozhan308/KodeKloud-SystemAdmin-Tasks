*Task


***There is a critical issue going on with the Nautilus application in Stratos DC. 
***The production support team identified that the application is unable to connect to the database. 
***After digging into the issue, the team found that mariadb service is down on the database server.


*MariaDB troubleshooting


**Connect to the datab

** 1. First try to check status of the mentioned service.

#sudo systemctl status mariadb

** 2. Then try to check logs of mariadb and check permissions 

#cd /var/log/mariadb/

**check ownership of logs and mysql folders

***Note : For mysql related logs and folders, the ownership should be mysql:mysql

#cd /var/lib/
#chown mysql:mysql mysql/

(or)

#cd /var/run/mariadb/
#chown mysql:mysql *
