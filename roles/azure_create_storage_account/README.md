<!-- This was created with Claude Code -->

azure_create_storage_account
============================

An Ansible role for azure create storage account.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **storage_account_names**: Variable used in: {{ item }}
  - Default: `{{ storage_account_name.split(',') }}`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_create_storage_account
      vars:
        storage_account_names: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
