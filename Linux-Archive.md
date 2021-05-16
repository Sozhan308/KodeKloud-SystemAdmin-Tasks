# Task

---

### On Nautilus storage server in Stratos DC there is a storage location /data which is used by different developers to keep their data (no confidential data). 
### One of the developers ravi has raised a ticket and asked for a copy of his/her data present in /data/ravi directory on storage server. 
### /home is an FTP location on storage server where developers can download their data. Below are the instructions shared by the system admin team to accomplish the task:

### a. Make a ravi.tar.gz compressed archive of /data/ravi directory and move the archive to /home directory on Storage Server.

---

**_Solution_**

1. login (SSH) to the storage server (ststor01)

`ssh username@ststor01`

2. compress the contents of the directory as ravi.tar.gz

`tar -czvf ravi.tar.gz /data/ravi/`

3. Move the archive to /home directory

`mv ravi.tar.gz /home/`

---