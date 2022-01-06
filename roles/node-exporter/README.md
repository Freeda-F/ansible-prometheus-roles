Role Name
=========

This is a role for installing and configuring Node expoters in 2 instances.

Requirements
------------

To configure and enable the node-exporter, we will be using [node_exporter.service](https://github.com/Freeda-F/ansible-prometheus-roles/tree/main/roles/node-exporter/files)

Role Variables
--------------

The varuables used are :
```
node_url: "https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz" #-----URL to download node exporter -----#
version_node: "1.3.1.linux-amd64" #-----Node exporter version-----#
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: nodes
      roles:
         - node-exporter

