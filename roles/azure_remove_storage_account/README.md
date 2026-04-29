<!-- This was created with Claude Code -->

azure_remove_storage_account
============================

An Ansible role for azure remove storage account.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **storage_account_names**: Resource name
  - Default: `{{ storage_account_name.split(',') }}`

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
    - role: azure_remove_storage_account
      vars:
        storage_account_names: <value>
        resource_group_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
