### MariaDB troubleshooting

**There is a critical issue going on with the Nautilus application in Stratos DC.**
**The production support team identified that the application is unable to connect to the database.**
**After digging into the issue, the team found that mariadb service is down on the database server.**

---

**_Solution_**

1. Connect to the database server

2. Verify the status of the mariadb service.

```sudo systemctl status mariadb```

3. Verify logs of mariadb and check permissions of the folders 

```cd /var/log/mariadb/```
```ls -l```

4. check ownership of logs and mysql folders

***_Note : For mysql related logs and folders, the ownership should be mysql:mysql_***

```cd /var/lib/```
```chown mysql:mysql mysql/```

_(OR)_

```cd /var/run/mariadb/```
```chown mysql:mysql```
