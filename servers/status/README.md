# Status

Hosted on `vps02.protokolla.fi`. The service is based on statping.

## Deploy to Oracle

Make sure you are in the root folder of this repo.

Run command

```sh
ansible-playbook -i inventory.ini servers/status/deploy.yml --become
```