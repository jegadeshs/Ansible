# Ansible Role: node exporter

## Description

Deploy prometheus [node exporter](https://github.com/prometheus/node_exporter) using ansible.

## Requirements

- Ansible >= 2.4

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `node_exporter_version` | 0.16.0 | Node exporter package version |
| `node_exporter_web_listen_address` | "0.0.0.0:9100" | Address on which node exporter will listen |

## Example

### Playbook

Use it in a playbook as follows:

---
- hosts: '{{ target }}'
  roles:
    - role: '{{ location }}'

### Execute

---
$ ansible-playbook run.yml --extra-vars "target=127.0.0.1 location=Prometheus/node_exporter"
