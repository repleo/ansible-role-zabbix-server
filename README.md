Ansible role - Zabbix Server Monitor installer
=====

[![Build Status](https://travis-ci.org/repleo/ansible-role-rainloop.svg?branch=master)](https://travis-ci.org/repleo/ansible-role-rainloop)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-repleo.rainloop-660198.svg?style=flat)](https://galaxy.ansible.com/repleo/rainloop)

This role install and configures zabbix-server. Zabbix is the ultimate enterprise-class monitoring platform.
Zabbix is the ultimate enterprise-level software designed for real-time monitoring of millions of metrics collected from tens of thousands of servers, virtual machines and network devices.

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------

```yaml
# General config.
zabbix_server_hostname: zabbix

# SSL Configuration.
zabbix_server_ssl: no
zabbix_server_redirect_http_to_https: yes
zabbix_server_ssl_certificate: "/etc/nginx/ssl/zabbix.crt"
zabbix_server_ssl_certificate_key: "/etc/nginx/ssl/zabbix.key"

# Database config.
zabbix_server_db_user: zabbix
zabbix_server_db_password: zabbix
zabbix_server_db_host: localhost
zabbix_server_db_name: zabbixdb

# defaults file;
# zabbix role specific

zabbix_server_version: 3.0
zabbix_server_timezone: Europe/Amsterdam
zabbix_server_repo: zabbix
zabbix_server_vhost: True
zabbix_server_web: true
zabbix_server_database_creation: True
zabbix_server_database_sqlload: True

# Database
zabbix_server_database_type: pgsql
zabbix_Server_database_type_long: postgresql
```

See defaults/main.yml for more options.

Dependencies
------------

- repleo.nginx
- repleo.postgresql

Example Playbook
----------------

Install rainloop
```yaml
- { role: repleo.zabbix-server }

```

License
-------

GPL v3 - (c) 2016, Repleo, Amstelveen

Author Information
------------------

Repleo, Amstelveen, Holland -- www.repleo.nl  
Jeroen Arnoldus (jeroen@repleo.nl)


