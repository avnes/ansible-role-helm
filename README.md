# ansible-role-helm

![Ansible](https://github.com/avnes/ansible-role-helm/actions/workflows/ansible.yaml/badge.svg)

Ansible role for installing helm.

## Requirements

Poetry. Install it from <https://python-poetry.org/docs/>

## Role Variables

```yaml
helm_version: latest     # It can also be a specifik version like v1.21.4
helm_for_all_users: true # If false it will install in in the users ~/bin directory
command_shell: bash         # Must be bash or zsh
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
     - { role: avnes.helm }
```

## For pip compability

```bash
poetry export --dev --output requirements.txt
```

## Test

```bash
poetry install
poetry shell
molecule test
```

## License

MIT

## Author Information

<https://github.com/avnes>
