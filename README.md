[![Build Status](https://travis-ci.org/alesium/ansible-www-tomcat.svg?branch=master)](https://travis-ci.org/alesium/ansible-www-tomcat)

www-tomcat
=========

Ansible Role to configure tomcat from pkgsrc

Requirements
------------

- Hosts requires pkgsrc's pkgin
- Hosts should be bootstrapped for ansible usage (have python,...)
- Root privileges, eg `become: yes`

Role Variables
--------------

| Variable | Description | Default value |
|----------|-------------|---------------|
| `www_tomcat_service_name` | Service name for handler | `"pkgsrc/tomcat"` | 
| `www_tomcat_setenv_sh_src` | setenv.sh source file location | `"setenv.sh.j2"` | 
| `www_tomcat_setenv_sh_dest` | setenv.sh remote location | `"/opt/local/share/tomcat/bin/setenv.sh"` | 

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: alesium.www-tomcat }

License
-------

BSD

Author Information
------------------

Sebastien Perreault <sperreault@alesium.net>
