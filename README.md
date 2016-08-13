# Linux-Server-Configuration
Linux deployment of a web application using PostgreSQL, Python, and Flask framework, in a Linux environment.

---
Linux distribution on a virtual machine, prepared to host web applications, install updates and securing it from a number of attack vectors.

This Project is in fulfilment of the Project 5 [Udacity Full Stack Web Developer Nanodegree Program](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004). It deploys Project 3 "Item Catalog App" on the virtual machine of Amazon Web Serices. 

Table of Contents
- [Project Access]
- [Project Overview]
- Installed Packages
- Configuration Summary
- Project Step by StepWalkthrough

---

**IP Address**

52.42.109.39

**SSH Port **

2200

**Non root User**

grader

**User `grader` credentials**

Train200

**Public access URL**

http://ec2-52-42-109-39.us-west-2.compute.amazonaws.com/

### Project Overview

The configuration of a Linux Ubuntu distribution is in a secured remote virtual machine in Amazon Web Service (AWS).  This deployment host a PostgreSQL database built trough ORM using a Flask Framework application.  

---

### Installed Packages

|**Package Name**|**Description**|
|:---------------:|:---------------:|
| Finger| Display in very readable format, the information about system users in AWS.|
| Apache2| HTTP server.|
| Libapache2-mod-wsgi |  Configuration library to host Python applications in Apache2 server.|
| Ntp|Synchronizes time over a network.|
| PostgreSQL|RDBs server for PostgreSQL.|
| Git| Version control.|
| Sqlalchemy|ORM and SQL tools for Python.|
| Flask|Microframework for web applications.|
| Python-psycopg2|PostgreSQL adapter for Python.|
| Oauth2|Authorization framework for third-party login (Google and Facebook).|
| Google-api-python-client|	Google API for OAuth login.|

---

###Configuration Summary

Setup AWS and SSH into the server.
A new system user grader was created with permission to `sudo`.
Curently installed packages were updated and upgraded.
Changed SSH Port from 22 to 2200 and configure SSH access.
Configured UFW (AWS firewall) to only allow incoming connections for SSH(Port:2200), HTTP(Port:80) and NTP(Port:123).
Configured local Time Zone to UTC.
Installed and configure Apache to serve a Python mod_wsgi application.
Installed Git and Setup Environment for delopying Flask Application.
Install and configure PostgreSQL with default settings to not allow remote connection.
Created a new user catalog, added user to PostgreSQL database with limited permissions to catalog application database.
Get OAUTH2 Logins (Google+ and Facebook) working.
