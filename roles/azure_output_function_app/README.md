<!-- This was created with Claude Code -->

azure_output_function_app
=========================

An Ansible role for azure output function app.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **functionappnames**: Variable used in: Gather functionapp group names
  - Default: `[]`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_output_function_app
      vars:
        functionappnames: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
