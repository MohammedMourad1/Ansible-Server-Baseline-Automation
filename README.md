# Ansible Role-Based Automation

## Overview

This project provides a **role-based Ansible automation framework** designed to configure and manage Linux servers in a clean, reusable, and scalable way.

The main focus of this project is to demonstrate:
- Proper usage of Ansible Roles
- Clean project structure following best practices
- Separation of configuration from execution logic
- Reusable automation suitable for real-world DevOps environments

---

## Project Objective

The goal of this project is to automate the creation of a **consistent server baseline** for Linux systems.

Instead of writing monolithic playbooks, this project uses **Ansible Roles** to:
- Improve maintainability
- Enable reusability across environments
- Make automation easier to extend and reason about

---

## Features

- Modular role-based architecture
- Centralized server baseline configuration
- Variable-driven design for flexibility
- Idempotent execution using Ansible best practices
- Ready to be extended with additional roles (security, monitoring, hardening)

---

## Project Structure

The project is organized as follows:

- `roles/`  
  Contains all Ansible roles used in the project

- `roles/server-baseline/`  
  Implements the baseline configuration for Linux servers

- `inventory/`  
  Defines target hosts and groups

- `site.yml`  
  Main playbook that applies roles to target hosts

This structure keeps the project clean and easy to scale as new roles are added.

---

## Included Roles

### Server Baseline Role

The `server-baseline` role is responsible for:
- Applying basic system configuration
- Installing commonly required packages
- Managing essential services
- Enforcing consistent baseline settings

Detailed documentation for this role is available inside:
- `roles/server-baseline/README.md`

---

## Requirements

Before running this project, ensure the following requirements are met:

- Ansible installed on the control machine
- SSH access to target servers
- Python available on target hosts
- A properly configured inventory file

---

## How to Run the Project

Follow these steps to execute the Ansible project:

### Step 1: Clone the Repository

Clone the project to your local machine:

- git clone https://github.com/MohammedMourad1/Ansible-role-based-automation.git
- cd Ansible-role-based-automation

---

### Step 2: Configure Inventory

Edit or create an inventory file to define your target hosts.

Example structure:
- inventory/hosts

Ensure SSH access is properly configured for the target servers.

---

### Step 3: Review Variables

Review default variables located in:
- roles/server-baseline/defaults/main.yml

Override variables if needed to match your environment.

---

### Step 4: Run the Playbook

Execute the main playbook using Ansible:

- ansible-playbook site.yml -i inventory/hosts

Ansible will connect to the target hosts and apply the defined roles.

---

## Verification

After execution, you can verify the results by:
- Checking installed packages
- Ensuring required services are running
- Confirming system configuration changes were applied successfully

---

## Use Cases

This project can be used for:
- Preparing newly provisioned servers
- Enforcing consistent configurations across environments
- Learning and demonstrating Ansible role-based automation
- Serving as a foundation for larger DevOps automation projects

---

## Future Improvements

Possible enhancements include:
- Adding security hardening roles
- Supporting additional Linux distributions
- Integrating monitoring and logging roles
- Introducing CI testing for roles

---

## Author

Mohammed Ahmed Mourad  
DevOps Engineer

---

## License

MIT

