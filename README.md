# ansible-role-zabbix-agent2

This role installs zabbix_agent2.

Supported OS:
 - Debian 12
 - Debian 11

Supported zabbix_agent2 versions: 6.0 to 7.4

---

## Installation

Edit **requirements.yml** file:

```yaml
roles:
  - name: zabbix_agent2
    src: https://github.com/lukaskaplan/ansible-role-zabbix-agent2.git
```

## Configuration

All config options are described in the `defaults/main.yml` file.

## Usage

Example of ansible **playbook.yml**

```yaml
- name: Zabbix_agent2 installation
  hosts: host

  tasks:
    - name: Role zabbix_agent2
      ansible.builtin.include_role:
        name: zabbix_agent2
      vars:
        zabbix_agent2_version: 7.2
        zabbix_agent2_server: x.x.x.x
        zabbix_agent2_serveractive: x.x.x.x
```

Run it:

```bash
ansible-playbook playbook.yml
```