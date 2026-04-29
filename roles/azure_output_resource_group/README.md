<!-- This was created with Claude Code -->

azure_output_resource_group
===========================

An Ansible role for azure output resource group.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **resourcegroupnames**: Variable used in: Gather resource group names
  - Default: `[]`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_output_resource_group
      vars:
        resourcegroupnames: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
