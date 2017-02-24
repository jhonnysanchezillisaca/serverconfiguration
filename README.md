Server Configuration
=====================
## Overview
Configuration of a server instance in  [Amazon Lightsail](https://lightsail.aws.amazon.com/) to host [MarketGardenLog](https://github.com/jhonnysanchezillisaca/marketgardenlog) web application.

The server is running on IP `54.88.202.235`. The SSH port is `2200`.
The hosted application is accesible via http://54.88.202.235/

## Software installed and configuration

### Machine's configuration
The server runs on Ubuntu 16.04.2 LTS. The machine's firewall only allows SSH connections on port `2200`, NTP connections on port `123` and HTTP on port `80`.

The root login via SSH is deactivated, and key-based SSH authentication is enforced.

The local timezone is configured to UTC.

### Software installed
- [Apache HTTP Server](https://httpd.apache.org/)
- [libapache2-mod-wsgi](http://packages.ubuntu.com/trusty/libapache2-mod-wsgi) (Python WSGI adapter module for Apache)
- [PostgreSQL](https://www.postgresql.org/)
- [Git](https://git-scm.com/)
- [Virtualenv](https://virtualenv.pypa.io/) (tool to create isolated Python environments)
- [Flask](http://flask.pocoo.org/)
- Project's dependencies
    - httplib2
    - requests
    - sqlalchemy
    - python-psycopg2
    - oauth2client

### Other configurations and third-party resources
To configure the web server to serve the Item Catalog application as a WSGI app we follow the Digital Ocean's tutorial on [How To Deploy a Flask Application on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)

To configure the PostgreSQL database to be used by the application we use the Digital Ocean's tutorial on [How To Secure PostgreSQL on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps) and Kill The Yak's tutorial on [use PostgreSQL with Flask or Django](http://killtheyak.com/use-postgresql-with-django-flask/)
