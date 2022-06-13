ansible_dhcpd
=========

Ansible role to generate configuration for simply DHCP server

Requirements
------------

1. Vagrant
2. libvirt

Role Variables
--------------

**Global configuration**

- domain_name_servers
- default_lease_time
- max_lease_time
- subnet
- netmask
- broadcast_address
- domain_name
- routers

**Define hosts with static ip addresses**

```
hosts_with_staticIP:
  name: <Name of machine>
  mac: 'xx:xx:xx:xx:xx:xx'
  ip: '192.168.x.x'
```

Example Playbook
----------------

```
---
- hosts: all
  become: yes
  roles:
    - dhcpd

```
