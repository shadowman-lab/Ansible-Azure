<!-- This was created with Claude Code -->

azure_compare_storage_account
=============================

An Ansible role for azure compare storage account.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **storageaccountnames**: Variable used in: Gather storage account names
  - Default: `[]`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_compare_storage_account
      vars:
        storageaccountnames: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
