build_report_cloud
========

Installs Apache and creates a report based on facts from a cloud provider.

Requirements
------------

Must run on Apache server

Role Variables / Configuration
--------------

N/A

Dependencies
------------

N/A

Example Playbook
----------------

The role can be used to create an html report on cloud statistics on any number of Linux hosts.


```
---
- name: Create Cloud Report
  hosts: all
  tasks:
  
    - name: Scan packages (Unix/Linux)
      ansible.builtin.package_facts:
      register: result
      when: ansible_os_family != "Windows"

    - name: Organize results for loopings
      ansible.builtin.set_fact:
        packagefacts: "{{ result.ansible_facts.packages | dict2items }}"
        cacheable: true
      when: ansible_os_family != "Windows"

    - name: Scan services (Unix/Linux)
      ansible.builtin.service_facts:
      when: ansible_os_family != "Windows"

    - name: Build the report
      ansible.builtin.include_role:
        name: shadowman.reports.build_report_cloud
        apply:
          delegate_to: report.shadowman.dev
          run_once: true      
```
