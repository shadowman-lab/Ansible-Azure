<!-- This was created with Claude Code -->

azure_gather_image_facts
========================

An Ansible role for azure gather image facts.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **location**: Variable used in: Image facts
  - Default: `eastus`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_gather_image_facts
      vars:
        location: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
