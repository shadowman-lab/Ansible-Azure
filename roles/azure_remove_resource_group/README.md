<!-- This was created with Claude Code -->

azure_remove_resource_group
===========================

An Ansible role for azure remove resource group.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **location**: Configuration parameter for azure_remove_resource_group
  - Default: `eastus`

* **resource_group_names**: Variable used in: {{ item }}
  - Default: `{{ resource_group_name.split(',') }}`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_remove_resource_group
      vars:
        location: <value>
        resource_group_names: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
