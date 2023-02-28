# Status

Hosted on `vps02.protokolla.fi`. The service is based on statping.

Installation directory is `/opt/status`.

## Deploy to Oracle

Make sure you are in the root folder of this repo.

Run command

```sh
ansible-playbook -i inventory.ini status/deploy.yml --become
```