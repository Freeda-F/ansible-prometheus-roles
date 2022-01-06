Role Name
=========

This is a role for installing and configuring Grafana.

Requirements
------------

To install Grafana in Amazon-linux instance, we will be using a custom grafana repository - [grafana.repo](https://github.com/Freeda-F/ansible-prometheus-roles/tree/main/roles/grafana/files)

Role Variables
--------------

The varuables used are :
```
monitor_ip: "65.2.149.51"  #---------grafana server IP---------#
grafana_user: admin  #---------grafana username---------#
grafana_password: admin123  #---------grafana password---------#
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: monitor
      roles:
         - grafana

