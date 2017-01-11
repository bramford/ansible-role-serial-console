# Ansible Role: serial-console

[![Build Status](https://travis-ci.org/bramford/ansible-role-serial-console.svg?branch=master)](https://travis-ci.org/bramford/ansible-role-serial-console)

Ansible role that configures grub to provide a tty on the serial interface (ttyS0) for Debian, RHEL/CentOS and Ubuntu.

## Supported Operating Systems

- RHEL/CentOS 7
- Debian 7/8
- Debian 9 (current debian 'testing' release)
- Ubuntu 12.04+ (untested)

## Requirements

- Ansible 2.1+

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { serial-console }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with optional vars set
      hosts: all
      roles:
        - { serial-console,
            serial_console_show_grub_menu: no
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/bramford/ansible-role-serial-console.git roles/serial-console
