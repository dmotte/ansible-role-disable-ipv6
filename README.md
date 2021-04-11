# ansible-role-disable-ipv6

Ansible role to **disable IPv6** completely on Debian/Ubuntu hosts.

TODO badges
TODO link ansible galaxy
TODO

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your *Ansible Playbook* like this:

   ```yaml
   - name: Include the dmotte.disable_ipv6 role
     include_role: { name: dmotte.disable_ipv6 }
     vars: { ansible_become: yes }
   ```

> **Note**: this role must be run as root (`ansible_become: yes`), because it needs to be able to use the `sysctl` command.
