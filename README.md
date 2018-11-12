# Udacity-Linux-Configuration
Installation of a Linux server and preparation to host web application deployment on it. 

### Cloud Partner
For this project I chose Amazon light-sail. 

### Environment: Server setup
- Followed [DigitalOcean Initial Server Setup with Ubuntu 16.04 tutorial](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04).
- Logged in as root, from light-sail using web browser
- Updated all currently installed packages
- Generated a private key using `ssh-keygen` tool and added it to the `ssh-agent`
- Copy SSH Key to Server using `ssh-copy-id`

## User setup
- Created a `grader` user for the Udacity grader with sudo rights.
- Created an SSH key pair for `grader` using the `ssh-keygen` tool.

## Security
- Configured the local timezone to UTC.
`sudo dpkg-reconfigure tzdata`
- Changed the SSH port from 22 to 2200
- Configured and enabled firewall
current firewall status

```text
Status: active
To                         Action      From
--                         ------      ----
80/tcp                     ALLOW       Anywhere                  
123/tcp                    ALLOW       Anywhere                  
2200/tcp                   ALLOW       Anywhere                  
Nginx HTTP                 ALLOW       Anywhere                  
Nginx Full                 ALLOW       Anywhere                  
80/tcp (v6)                ALLOW       Anywhere (v6)             
123/tcp (v6)               ALLOW       Anywhere (v6)             
2200/tcp (v6)              ALLOW       Anywhere (v6)             
Nginx HTTP (v6)            ALLOW       Anywhere (v6)             
Nginx Full (v6)            ALLOW       Anywhere (v6)   
```

## Application Functionality
Item Catalog application can found https://github.com/Shahroz16/Item-catalog,

Following functionalities has been added 

* `Web Server` 
* `WSGI`
* `PostgreSQL`

## IP Address

35.154.94.175

## URL

http://35.154.94.175.xip.io/

## Summary of Software

* `Python`
* `Flask` 
* `SQLAlchemy`
* `Nginx`
* `Uwisgi`
* `PostgreSQL`

## Note
'Authentication' is not functional right now, but since it's not a requirement for this project I am going to delay it a bit.
