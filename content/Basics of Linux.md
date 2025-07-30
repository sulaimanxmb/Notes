#### Sensitive Files :
- `/etc/passwd`: Contains user account information. It's readable by all users but doesn't store passwords (passwords are stored in `/etc/shadow`).

- `/etc/shadow`: Contains hashed passwords for user accounts. It is readable only by the root user.     

- `/var/log/auth.log`: Contains authentication-related messages, such as login attempts, use of ***sudo***, and other security-related events.

- `/var/log/apache2/`: Contains logs for Apache HTTP server activities, including access logs and error logs.

- `/proc/self/environ/`: It contains Information about the environment ( Browser ).

#### Terminal Commands :
Some of the Commands are here : [[Linux Commands.pdf]]

#### Architecture of Linux :
The kernel manages all the permissions from application/user to access the hardware

![[architecture-of-linux.png]]

#### Web server :
Getting the web server up in kali linux :
```bash
sudo systemctl start apache2
```

On macos :
```bash
sudo apachectl start
sudo apachectl stop
```
