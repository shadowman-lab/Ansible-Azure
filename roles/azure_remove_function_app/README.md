<!-- This was created with Claude Code -->

azure_remove_function_app
=========================

An Ansible role for azure remove function app.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **functionapp_names**: Variable used in: {{ item }}
  - Default: `{{ functionapp_name.split(',') }}`

* **resource_group_name**: Variable used in: {{ item }}
  - Default: `Demo`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_remove_function_app
      vars:
        functionapp_names: <value>
        resource_group_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
