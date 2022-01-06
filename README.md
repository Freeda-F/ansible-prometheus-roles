# Prometheus-NodeExporter-Grafana deployment using Ansible roles

Prometheus is an open-source monitoring system which is very lightweight and has a good alerting mechanism. Prometheus can monitor hundreds of instances and display metrics and statistics from all of them to you in one simple dashboard. 

Grafana is a web application that gives you visualization tools. In a nutshell, we will be able to create and use dashboards from Grafana to visualize all the statistics and metrics presented by Prometheus.

## Project Scope

In this demo, we will be creating an Ansible playbook to automate the installation of grafana, node_exporter, and Prometheus into an EC2 instance. Here, we will be making use of ansible roles to deploy each components.

## Architecture

This is a monitoring project which consists of the following components:

- Node Exporter : Node exporter produces metrics about infrastructure which include CPU, memory, disc, network stats etc.
- Prometheus : It helps monitor servers which are called targets. It can be a single target or multiple targets monitored for different metrics.
- Grafana : Is a tool for visualising the metrics by connecting with the prometheus server.

In this module, we will see how each of these components can be automatically deployed using ansible playbook.

![image](https://user-images.githubusercontent.com/93197553/148266068-81e63e4f-744e-4bf1-9dde-734486b7ecb4.png)

We will be deploying this project using 3 instances.

- In the first instance, we will be setting this up as a monitoring server in which we will be installing prometheus(port:9090) and Grafana(port:3000) application. This instance connects to other 2 instances and reads the metrices like cpu usage,memory, stats etc in a timely manner.

- In the other 2 nodes, we will be setting up the node exporter which will be working on port 9100.

## Requirements

- Install Ansible on your machine (ansible master).
- Ansible-galaxy
- 3 instances for installing node exporter, prometheus and grafana applications.

## Variables used

```
node_url: "https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz" ## binary for node-exporter
version_node: "1.3.1.linux-amd64" ## version for node-exporter
prometheus_url: "https://github.com/prometheus/prometheus/releases/download/v2.32.1/prometheus-2.32.1.linux-amd64.tar.gz" ## binary for prometheus
version_prom: "2.32.1.linux-amd64" ## version for prometheus
node_ip1: "3.108.3.4" ## public IP for node-exporter-1
node_ip2: "13.233.3.4" ## public IP for node-exporter-2
monitor_ip: "3.110.3.4" ## public IP for prometheus and grafana installed server
grafana_user: admin ## grafana username
grafana_password: admin123 ## grafana password

```

## Provisioning


## Results




