# ansible-role-pocketbase

## Requirements

Ansible 2.9 or higher.

## Variables

Variables and defaults for this role.

### defaults/main.yml

```yaml
pocketbase_role_enabled: false
```

## Dependencies

None.

## Example Playbook

```yaml
---
# role: ansible-role-pocketbase
# play: pocketbase
# file: pocketbase.yml

- hosts: all
  become: true
  gather_facts: true
  vars:
    pocketbase_role_enabled: true
  roles:
    - role: ansible-role-pocketbase
```
