<!-- This was created with Claude Code -->

azure_bespoke
=============

An Ansible role for azure bespoke.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **azure_savings_perform_savings**: Configuration parameter for azure_bespoke
  - Default: `True`

* **azure_savings_untagged**: Variable used in: {{ instance_info.vms | rejectattr('tags') | map(attribute='name') | list }}
  - Default: `True`

* **azure_savings_no_owner**: Variable used in: {{ instance_info.vms | selectattr('tags.owner', 'undefined') | map(attribute='name') | list }}
  - Default: `True`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_bespoke
      vars:
        azure_savings_perform_savings: <value>
        azure_savings_untagged: <value>
        azure_savings_no_owner: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
