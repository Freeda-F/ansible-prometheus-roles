Role Name
=========

This is a role for installing and configuring prometheus application in an instance.

Requirements
------------

To configure and enable the prometheus, we will be using [prometheus.service](https://github.com/Freeda-F/ansible-prometheus-roles/tree/main/roles/prometheus/files)

Role Variables
--------------

The varuables used are :
```
prometheus_url: "https://github.com/prometheus/prometheus/releases/download/v2.32.1/prometheus-2.32.1.linux-amd64.tar.gz" ## URL for downloading prometheus
version_prom: "2.32.1.linux-amd64" ## version for prometheus
node_ip1: "3.110.147.219" ## public IP for node-exporter-1
node_ip2: "13.232.225.117" ## public IP for node-exporter-2
monitor_ip: "65.2.149.51" ## public IP for prometheus and grafana installed server
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: monitor
      roles:
         - prometheus

