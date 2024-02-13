### Assignment

1.  Creation of *altschool* login user with home directory: `sudo useradd -m Altschool`
2.  Set the password for *altschool* user:  `sudo passwd altschool` `password: altschool`
3.  Login to *altschool* user account : `su  altschool`
4.  Create the requested directories (_code, tests, personal and misc_): `mkdir code tests personal misc`

  



###  Solutions:

|  | Description | Commands |
|--------|------------|----------|
| a      | Change directory to the tests directory using absolute pathname                 | `cd /home/altschool/tests`     |
| b      | Change directory to the tests directory using relative pathname                  | `cd tests`         |
| c      | Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory                  | `echo "Hello A" > /home/altschool/misc/fileA`          |
| d      | Create an empty file named fileB in the misc directory                  | `touch /home/altschool/misc/fileB`         |
| e      | Copy contents of fileA into fileC                  | `cp /home/altschool/misc/fileA /home/altschool/misc/fileC`         |
| f      |  Move contents of fileB into fileD                | `mv /home/altschool/misc/fileB /home/altschool/misc/fileD`          |
| g      | Create a tar archive called misc.tar for the contents of misc directory                  | `tar -cvf misc.tar misc`          |
| h      | Compress the tar archive to create a misc.tar.gz file  | `gzip misc.tar`         |
| i      | Create a user and force the user to change his/her password upon login                 |i. create new user: _tricia_ `sudo useradd tricia` <br> ii. force **tricia** password change on login: `sudo passwd -e tricia`         **or** `sudo chage -d 0 tricia`|
| j      | Lock a users password | `sudo passwd -l tricia`         |
| k     | Create a user with no login shell                 |  `sudo useradd -s /usr/sbin/nologin daniel`        |
| l     | Disable password based authentication for ssh                  | Use `sudo vim /etc/ssh/sshd_config` and set `PasswordAuthentication no`       | 
| m     | Disable root login     | Use `sudo vim /etc/ssh/sshd_config` and set `PermitRootLogin no`          |
