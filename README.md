Ansible role: zabbix_agent2
=========

[![CI](https://github.com/lukaskaplan/ansible-role-zabbix-agent2/actions/workflows/ci.yml/badge.svg)](https://github.com/lukaskaplan/ansible-role-zabbix-agent2/actions/workflows/ci.yml)

Ansible role which installs zabbix_agent2. It makes a basic confogration too.

Supported zabbix_agent2 versions: `6.0` to `7.4`

Requirements
------------

Supported OS:

- Debian 12
- Debian 11

Role Variables
--------------

All config options are described in the `defaults/main.yml` file.

Dependencies
------------

None

Installation
------------

Edit **requirements.yml** file:

```yaml
roles:
  - name: zabbix_agent2
    src: https://github.com/lukaskaplan/ansible-role-zabbix-agent2.git
```

```bash
ansible-galaxy install -r requirements.yml
```

Example Playbook
----------------

File **playbook.yml**:

```yaml
- name: Example playbook
  hosts: servers

  tasks:
    - name: Role zabbix_agent2
      ansible.builtin.include_role:
        name: zabbix_agent2
      vars:
        zabbix_agent2_version: 7.2
        zabbix_agent2_server: x.x.x.x
        zabbix_agent2_serveractive: x.x.x.x
```

How to run it:

```bash
ansible-playbook playbook.yml
```

License
-------

MIT

Author Information
------------------

This role was created by [Lukas Kaplan](https://lkaplan.cz).
