# ansible-apps_jdk11

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_jdk11-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_jdk11)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_jdk11.svg)](https://github.com/lotusnoir/ansible-apps_jdk11/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_jdk11?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_jdk11)
[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/lotusnoir/apps_jdk11)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/lotusnoir/apps_jdk11)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Description](#description)
- [Requirements](#requirements)
- [Role variables](#role-variables)
- [Examples](#examples)
- [License](#license)
- [Author Information](#author-information)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Description

Install anc configure BMC control-M agent in order to launch cron tasks

## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

As the package cannot be downloaded by a public link, you need to provide a path or url in order to install it, with default variables, this role dont change anything on the system. You need to set the config variables like in the exemple in order to start configuration.


vars:
  controlm_agent_install_method: url # or file
  controlm_agent_install_url: "http://downloadpackage/xxxxxxxxx"
  controlm_agent_primary_server: "servername.exemple.fr"
  controlm_agent_auth_server: "servername.exemple.fr"

## Examples

        ---
        - hosts: apps_jdk11
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_jdk11

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
