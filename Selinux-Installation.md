# Selinux - installation

---

### Install the required packages of SElinux on App server 1 in Stratos Datacenter and disable it permanently for now; it will be enabled after ### making some required configuration changes on this host. Don't worry about rebooting the server as there is already a reboot scheduled for ### tonight's maintenance window. 
### Also ignore the status of SElinux command line right now; the final status after reboot should be disabled.

---

**_Solution_**

---

1. Verify for installed packages related to SElinux

`rpm -qa | grep -i selinux`

2. Install the below packages

`sudo yum install selinux-policy-targeted selinux-policy-devel -y`
`sudo yum install policycoreutils policycoreutils-python setools setools-console setroubleshoot -y`

3. After installed, Set SELINUX=disabled in /etc/selinux/config

---