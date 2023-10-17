Ansible Role: DHCP Server
=========

An Ansible role to set up a DHCP server in AD.

Requirements
------------

Access to a DC and DA credentials.

Role Variables
--------------

```yml
domain_pdc: pdc01
domain_name: ad01.bufu-sec.com
domain_admin_user: 'ad01\administrator'
domain_admin_password: Password!
dhcp_scope_name: Default
dhcp_scope_id: 192.168.91.0
dhcp_scope_start: 192.168.91.100
dhcp_scope_end: 192.168.91.254
dhcp_scope_subnet_mask: 255.255.255.0
dhcp_scope_dns_server: 192.168.91.2
dhcp_scope_gateway: 192.168.91.1
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: pdc01
  roles:
    - role: xbufu.ad_dhcp
      vars:
        domain_pdc: pdc01
        domain_name: ad01.bufu-sec.com
        domain_admin_user: 'ad01\administrator'
        domain_admin_password: Password!
        dhcp_scope_name: Default
        dhcp_scope_id: 192.168.91.0
        dhcp_scope_start: 192.168.91.100
        dhcp_scope_end: 192.168.91.254
        dhcp_scope_subnet_mask: 255.255.255.0
        dhcp_scope_dns_server: 192.168.91.2
        dhcp_scope_gateway: 192.168.91.1

```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
