# Netsoc Admin

## Purpose

This is intended to be a one-stop shop for users of UCC Netsoc's servers.

## Features

### We have:
* Automated user account creation
* MySQL database managment
* Backup managment
* Facility to contact a sysadmin
* WordPress installer
* Tutorials

### We will have:
* Server password reset functionality
* Own domain name linking to WordPress installation

## Installation

To build the docker image:

1. Create a file called `wordpress_installer_config.py` following the same format as of that in `sample_wordpress_installer_config.py`. This file configures the wordpress_installer package. 
2. Create a `admin_passwords.py` following the same format as of that in `sample_admin_passwords.py`. This file configures the netsoc admin server itself.

2. In this directory, run:
```
docker build -t netsocadmin .
```

To run the docker image:

`docker run --net="host" -v /path/to/backups:/backups -v /path/to/home/dirs:/home/users netsocadmin:latest`