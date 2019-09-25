# Ansible Role: mariadb-galera-cluster
=========

A simple Ansible role for installing and configuring the Zabbix Server for RHEL/CentOS 7.

- Install the necessary packages;
- Create configuration file;


Requirements
------------

- The SELINUX and firewall settings are not considered to be a concern of this role.

Role Variables
--------------


None of the variables below are required

| Variable                                     | Default                       | Comments                                                                                |
| :---                                         | :---                          | :---                                         
| `zabbix_password`                            |                               | zabbix user password
|                                              |                               |
| `zabbix_user`				                         |                               | zabbix user, default is zabbix
|                                              |                               |
| `your_timezone`                              |                               | configure your Timezone.
|                                              |                               |
| `root_login`                                 |                               | user root                                   |                                              |                               |
| `root_password`                              |                               | root password                               |                                              |                               |
| `zabbix_db`				                           |			                         | Database name, default is zabbix
|                                              |                               | 

Verify timezone in https://www.php.net/manual/en/timezones.php

Dependencies
------------

No dependencies.


Example Inventory File
----------------------
[zabbix]
192.168.0.23


Example Playbook
----------------

---
- hosts: zabbix
  become: yes
  roles:
    - /path/zabbix
...

Finish Configuration
--------------------
http://your_ip/zabbix/setup.php

After finish configuration default user and password below.
-----------------------------------------------------------
Username: "admin"
Password: "zabbix"

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido
