Ansible OpenVPN
===============

collection of Ansible roles to run OpenVPN.

Requirements
------------

Ubuntu 12.04 (Precise) or Ubuntu 14.04 (Trusty)

Content Roles
-------------

* **connection** - access network on the provisioned machine on another

Dependencies
------------

no other roles currently

Example Playbook
----------------

```yml
- hosts: vpn-target
  sudo: true
  sudo_user: root

  roles:
  - role: dresden-weekly.openvpn/connection
    openvpn_server_name: 'target_vpn'
    openvpn_server_device_ip: 10.10.1.1
    openvpn_client_device_ip: 10.10.1.2
    openvpn_client_routes:
    - '192.168.122.0 255.255.255.0'
```
