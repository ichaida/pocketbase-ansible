# Pocketbase Ansible

This is an Ansible Role installing Pocketbase on a Debian distribution, exposing the serivce behind a simple reverse proxy Nginx.

## Requirements

Ansible 2.9 or higher.

## Example Playbook

```yaml
---
# role: ansible-role-pocketbase
# play: pocketbase
# file: playbook.yml

- hosts: all
  become: true
  gather_facts: true
  vars:
    pocketbase_role_enabled: true
  roles:
    - role: ansible-role-pocketbase
```

## Usage

To try this Pocketbase playbook on your Debian server from your inventory file, run the following:

```shell
# Update your hosts file
cat hosts
# Replace the place holder 'DEBIAN-VM-IP' with your Debian VM's IP Address or Host Name
# Make sure to exchange SSH Keys between your Debian VM and the machine running the Ansible Playbook

# Setup Pocketbase on your Debian Machine
ansible-playbook playbook.yml -i hosts
```

**Important:**
Once playbook done, navigate to http://DEBIAN-VM-IP/\_/ in order to setup your Admin account.

## Code Styles

You can use `pre-commit` to align with Ansible best practices:

```shell
pip3 install pre-commit
pre-commit install
pre-commit run --all-files
```
