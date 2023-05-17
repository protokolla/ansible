# ansible
This repository contains all Ansible scripts used to manage protokolla.fi services.

## mirrors

This repository can be found on

- [protokolla.fi's Gitea](https://git.protokolla.fi/protokolla/ansible) - push your commits here
- [Github](https://github.com/protokolla/ansible/) - only a read-only mirror / resets every 15 min to gitea repos state

## Prepare all servers

## Metso

Decrypt the vault

```bash
ansible-vault decrypt vaults/servers/metso.yml.enc
```

Run the playbook

```bash
ansible-playbook -i inventory.ini playbooks/servers/metso.yml -e @vaults/servers/metso.yml.enc
```

Encrypt the vault

```bash
ansible-vault encrypt vaults/servers/metso.yml.enc
```

## Status page

Decrypt the vault

```bash
ansible-vault decrypt vaults/servers/status.yml.enc
```

Run the playbook

```bash
ansible-playbook -i inventory.ini playbooks/servers/status.yml -e @vaults/servers/status.yml.enc --become
```

Encrypt the vault

```bash
ansible-vault encrypt vaults/servers/status.yml.enc
```