<!-- This was created with Claude Code -->

# Azure Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Azure)


This directory contains Ansible automation for azure management and operations.

## Overview

The Azure automation provides playbooks and roles for managing and configuring
azure infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [azure_bespoke](roles/azure_bespoke/README.md) | Role for azure bespoke |
| [azure_compare_function_app](roles/azure_compare_function_app/README.md) | Role for azure compare function app |
| [azure_compare_resource_group](roles/azure_compare_resource_group/README.md) | Role for azure compare resource group |
| [azure_compare_storage_account](roles/azure_compare_storage_account/README.md) | Role for azure compare storage account |
| [azure_compare_vm](roles/azure_compare_vm/README.md) | Role for azure compare vm |
| [azure_create_function_app](roles/azure_create_function_app/README.md) | Role for azure create function app |
| [azure_create_resource_group](roles/azure_create_resource_group/README.md) | Role for azure create resource group |
| [azure_create_storage_account](roles/azure_create_storage_account/README.md) | Role for azure create storage account |
| [azure_create_vm](roles/azure_create_vm/README.md) | Role for azure create vm |
| [azure_gather_image_facts](roles/azure_gather_image_facts/README.md) | Role for azure gather image facts |
| [azure_gather_info](roles/azure_gather_info/README.md) | Role for azure gather info |
| [azure_opt_in_start](roles/azure_opt_in_start/README.md) | Role for azure opt in start |
| [azure_opt_in_stop](roles/azure_opt_in_stop/README.md) | Role for azure opt in stop |
| [azure_output_function_app](roles/azure_output_function_app/README.md) | Role for azure output function app |
| [azure_output_resource_group](roles/azure_output_resource_group/README.md) | Role for azure output resource group |
| [azure_output_storage_account](roles/azure_output_storage_account/README.md) | Role for azure output storage account |
| [azure_output_vm](roles/azure_output_vm/README.md) | Role for azure output vm |
| [azure_remove_function_app](roles/azure_remove_function_app/README.md) | Role for azure remove function app |
| [azure_remove_resource_group](roles/azure_remove_resource_group/README.md) | Role for azure remove resource group |
| [azure_remove_storage_account](roles/azure_remove_storage_account/README.md) | Role for azure remove storage account |
| [azure_remove_vm](roles/azure_remove_vm/README.md) | Role for azure remove vm |
| [azure_retrieve_info](roles/azure_retrieve_info/README.md) | Role for azure retrieve info |
| [azure_schedule_parking](roles/azure_schedule_parking/README.md) | Role for azure schedule parking |
| [azure_vm_gather_for_parking](roles/azure_vm_gather_for_parking/README.md) | Role for azure vm gather for parking |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| Functionapp_output.yml | Playbook for Functionapp output | localhost |
| azure_automation_save.yml | Playbook for azure automation save | localhost |
| azure_create_functionapp.yml | Playbook for azure create functionapp | localhost |
| azure_create_instance.yml | Playbook for azure create instance | localhost |
| azure_create_resourcegroup.yml | Playbook for azure create resourcegroup | localhost |
| azure_create_storageaccount.yml | Playbook for azure create storageaccount | localhost |
| azure_image_facts.yml | Playbook for azure image facts | localhost |
| azure_parking_schedule.yml | Playbook for azure parking schedule | localhost |
| azure_parking_start.yml | Playbook for azure parking start | localhost |
| azure_parking_stop.yml | Playbook for azure parking stop | localhost |
| azure_remove_functionapp.yml | Playbook for azure remove functionapp | localhost |
| azure_remove_instance.yml | Playbook for azure remove instance | localhost |
| azure_remove_resourcegroup.yml | Playbook for azure remove resourcegroup | localhost |
| azure_remove_storageaccount.yml | Playbook for azure remove storageaccount | localhost |
| buildazuredetailedreport.yml | Playbook for buildazuredetailedreport | localhost |
| buildazurereport.yml | Playbook for buildazurereport | localhost |
| functionapp_compare.yml | Playbook for functionapp compare | localhost |
| inventory_compare.yml | Playbook for inventory compare | localhost |
| inventory_output.yml | Playbook for inventory output | localhost |
| resource_group_compare.yml | Playbook for resource group compare | localhost |
| resourcegroup_output.yml | Playbook for resourcegroup output | localhost |
| storage_account_compare.yml | Playbook for storage account compare | localhost |
| storageaccount_output.yml | Playbook for storageaccount output | localhost |
| survey_create.yml | Playbook for survey create | all |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run Functionapp_output.yml

# Run in stdout mode
ansible-navigator run Functionapp_output.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - azure_bespoke
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-Azure/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
