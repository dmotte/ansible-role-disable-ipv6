# ansible-role-disable-ipv6

[![GitHub latest release](https://img.shields.io/github/v/release/dmotte/ansible-role-disable-ipv6?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-disable-ipv6/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.disable__ipv6-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/disable_ipv6)

Ansible role to **disable IPv6** completely on Debian/Ubuntu hosts.

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your _Ansible Playbook_. See [`test/playbook.yml`](test/playbook.yml) for an example of how to do that. Remember to replace the role name with `dmotte.disable_ipv6`.

> **Note**: this role must be run as root (`ansible_become: true`), because it needs to be able to use the `sysctl` command.

### Role variables

| Variable                   | Description                                                                                 |
| -------------------------- | ------------------------------------------------------------------------------------------- |
| `reload_sysctl_if_changed` | Whether or not to reload the sysctl configuration from disk if it changes (default: `true`) |

## Development

If you want to contribute to this project, you can use the [`test/playbook.yml`](test/playbook.yml) file to test the role while editing it.

Place your inventory file (e.g. `hosts.yml`) inside the `test` folder.

Edit the `vars` section of the [`test/playbook.yml`](test/playbook.yml) file to match your scenario.

You can then **execute the playbook** against your host:

```bash
cd test/
ansible-playbook -i hosts.yml playbook.yml
```
