<!-- This was created with Claude Code -->

azure_remove_vm
===============

An Ansible role for azure remove vm.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **publisher**: Configuration parameter for azure_remove_vm
  - Default: `RedHat`

* **offer**: Configuration parameter for azure_remove_vm
  - Default: `RHEL`

* **version**: Version number or identifier
  - Default: `7.8.2020050910`

* **sku**: Configuration parameter for azure_remove_vm
  - Default: `7.8`

* **vm_size**: Size specification
  - Default: `Standard_B1s`

* **vm_names**: Variable used in: {{ item }}
  - Default: `{{ vm_name.split(',') }}`

* **resource_group**: Variable used in: Remove instance
  - Default: `Demo`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_remove_vm
      vars:
        publisher: <value>
        offer: <value>
        version: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
