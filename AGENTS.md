# Agent Guidelines & Repository Structure Rules

## Directory Organization & Configuration File Placement
- **Ansible Configuration & Playbooks**: All Ansible configuration files, playbooks, roles, inventory files, and group variables must be placed in the `~/NM-FSM-App/devops-course` directory on the control node (and mirrored locally in `C:\code\NM-FSM-App\devops-course`).
- **Packer Configurations**: All Packer template and configuration files must be placed in the `~/NM-FSM-App/devops-course` directory.
- **Terraform Configurations**: All Terraform configuration files (`.tf`, `.tfvars`, state files, and modules) must be placed inside the Terraform subdirectory: `~/NM-FSM-App/devops-course/terraform/` (and mirrored in `C:\code\NM-FSM-App\devops-course\terraform`).

## Environment & Path Standards
- **Control Node**:
  - Base Directory: `~/NM-FSM-App/devops-course`
  - Ansible Config: `~/NM-FSM-App/devops-course/ansible.cfg`
  - Inventory: `~/NM-FSM-App/devops-course/hosts.ini`
  - Terraform Subdirectory: `~/NM-FSM-App/devops-course/terraform/`
- **Bastion Host**:
  - Base Directory: `C:\code\NM-FSM-App\devops-course`
  - Terraform Subdirectory: `C:\code\NM-FSM-App\devops-course\terraform`
- **Security & Vault Rules**:
  - Never commit vault password files (e.g. `.ansible_vault_pass`) to GitHub or version control.
  - Encrypted vault values in `group_vars` and `vault.yml` are tracked in version control.
