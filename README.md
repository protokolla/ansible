# Ansible
This repository contains all Ansible scripts used to manage protokolla.fi services. Service configurations and data is stored in `/opt/services` and everything is containerized.

## Mirrors

This repository can be found on

- [protokolla.fi's Gitea](https://git.protokolla.fi/protokolla/ansible) - push your commits here
- [Github](https://github.com/protokolla/ansible/) - only a read-only mirror / resets every 15 min to gitea repos state

These scripts are made with both amd64 and arm in mind. Everything should work the same on Oracle VPS as on a Hetzner dedi.

## Playbooks

### `setup.yml`

Use this to initialize server:

- set motd to match the `inventory.yml` file
- setup motd
- install some common packages that aren't installed by default on minimized Ubuntu or on Debian
- install docker and compose plugin
- update packages

```bash
ansible-playbook playbooks/setup.yml -i inventory.ini
```