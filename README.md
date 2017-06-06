# Linux-Server-Configuration

## Access Points

IP: **52.90.47.201**

Port: **2200**

Url: **[ec2-52-90-47-201.compute-1.amazonaws.com](ec2-52-90-47-201.compute-1.amazonaws.com)**

## Summary of software and configuration changes.

- Update all installed 
- Configure firewall (UFW)
  - default deny incoming
  - default allow outgoing
  - allow ssh
  - allow 2200/tcp
  - allow http
  - allow 123
- Change ssh port to 2200
- Create and configure user `grader`
  - add user `grader`
  - grant `grader` sudo permission
  - generate ssh key for `grader`
- Set server timezone to UTC
- Install software from Ubuntu packages
  - apache2
  - libapache2-mod-wsgi
  - postgresql
  - python-pip
- Setup `sites-enabled` file `FlaskApp.conf`
- Setup Postgre database
  - create user `catalog` with limited permission
  - create database `catalog`
- Clone [Item Catalog repository](https://github.com/TWHou/catalog)
- Install python packages
  - flask
  - sqlalchemy
  - oauth2client
  - requests

## Resources used
- [Setup Flask App on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
- [Setup PostgreSQL on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps)
- [Set Server Timezone](https://askubuntu.com/questions/323131/setting-timezone-from-terminal)