# ansible
This repository contains all Ansible scripts used to manage protokolla.fi services.

# Prepare all servers

# Status page

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