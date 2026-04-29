<!-- This was created with Claude Code -->

azure_create_vm
===============

An Ansible role for azure create vm.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **publisher**: Variable used in: Change facts if running Windows
  - Default: `RedHat`

* **offer**: Configuration parameter for ansible.builtin.set_fact task
  - Default: `rhel-byos`

* **version**: Variable used in: {{ item }}
  - Default: `latest`

* **sku**: Variable used in: Change facts if running Windows
  - Default: `rhel-lvm79`

* **vm_size**: Variable used in: {{ azureuser }}
  - Default: `Standard_B1s`

* **vm_names**: Variable used in: {{ sku | lower }}
  - Default: `{{ vm_name.split(',') }}`

* **resource_group_name**: Variable used in: Provision instance RHEL
  - Default: `Demo`

* **storage_account_name**: Variable used in: {{ item }}
  - Default: `demorh`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: azure_create_vm
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
