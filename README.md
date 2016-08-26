adriagalin.motd
===============

[![Build Status](https://travis-ci.org/adriagalin/ansible.motd.svg?branch=master)](https://travis-ci.org/adriagalin/ansible.motd) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-motd-blue.svg)](https://galaxy.ansible.com/list#/roles/4779)

An ansible role for configuring Message Of The Day (motd) file. By default this role add additional information about the distro and the hardware.

Requirements
------------

Tested on:

-	Ubuntu 14.04 LTS
-	Ubuntu 16.04 LTS
-	RHEL 6.7 Santiago
-	RHEL 7.2 Maipo
-	CentOS 7.2.1511 Core

Should work with:

-	All Ubuntu
-	All Debian
-	All RHEL
-	All Centos

Role Variables
--------------

```yaml
ag_motd_add_footer: false
ag_motd_sysadmins_signature: set sysadmin team signature
ag_motd_sysadmins_email: set sysadmin support email
ag_motd_content: set content of motd
ag_motd_info: additional information to show in message
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: adriagalin.motd }
```

This playbook produces the /etc/motd file looking like this:

```
--------------------------------------------------------------------------
                    This system is managed by Ansible
--------------------------------------------------------------------------

This is host1 running Debian.

NOTE: System and application configuration for this host is managed by
automated systems. To ensure that any changes you make here are not lost,
please contact with your system administrators.

 FQDN:    host1
 Distro:  Debian 7.8 wheezy
 Virtual: NO
 CPUs:    8
 RAM:     16.0GB

Yours,
Random system administrators
email: random@random.com

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

Last ansible run: 2015-08-12T23:09:07Z
```

License
-------

GPLv3 License.

Author Information
------------------

[Adrià Galín](http://www.adriagalin.com)

Inspiration
-----------

During development, some roles in Ansible Galaxy/Github also inspired me:

-	[michaelrigart](https://github.com/michaelrigart/ansible-role-motd)
-	[picotrading](https://github.com/picotrading/ansible-motd)
-	[geerlingguy](https://github.com/geerlingguy/ansible-role-mysql)
-	[nickjj](https://github.com/nickjj/ansible-locale)
-	and many others.

thank you.
