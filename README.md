Apache Install via Yum
=========

This role will install Apache on RPM based distributions (RHEL, CentOS, etc) using yum.

Role Variables
--------------

apache_server_admin - set in defaults/main.yml (replaces "ServerAdmin {{ apache_server_admin }}" line in httpd conf template, templates/httpd.conf.j2)

Example Playbook
----------------

```
---
- hosts: all
  become: yes
  roles:
    - apache
  vars: 
    apache_server_admin: your_email@domain.com
```

License
-------

BSD

Author Information
------------------

Ryan Smith!
