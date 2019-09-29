# Ansible Role: rabbitmq_exporter

[![Build Status](https://travis-ci.org/cimon-io/ansible-rabbitmq-exporter.svg?branch=master)](https://travis-ci.org/cimon-io/ansible-rabbitmq-exporter)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)

## Description

Deploy prometheus [rabbitmq exporter](https://github.com/kbudde/rabbitmq_exporter) using ansible.

## Requirements

- Ansible >= 2.6 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `rabbitmq_exporter_version` | 1.0.0-RC6.1 | RabbitMQ exporter package version. Also accepts latest as parameter. |
| `rabbitmq_exporter_system_group` | "rabbitmq-exp" | System group used to run rabbitmq_exporter |
| `rabbitmq_exporter_system_user` | "rabbitmq-exp" | System user used to run rabbitmq_exporter |
| `rabbitmq_exporter_env` | `{ PUBLISH_PORT: 9419 }` | Rabbitmq_exporter environment variables for configuration

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - cimon-io.rabbitmq-exporter
```

## License

This project is licensed under MIT License.
