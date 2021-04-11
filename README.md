# ansible-role-disable-ipv6

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dmotte/ansible-role-disable-ipv6/release?logo=github&style=flat-square)](https://github.com/dmotte/desktainer/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.disable__ipv6-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/disable_ipv6)

Ansible role to **disable IPv6** completely on Debian/Ubuntu hosts.

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your *Ansible Playbook* like this:

   ```yaml
   - name: Include the dmotte.disable_ipv6 role
     include_role: { name: dmotte.disable_ipv6 }
     vars: { ansible_become: yes }
   ```

> **Note**: this role must be run as root (`ansible_become: yes`), because it needs to be able to use the `sysctl` command.
