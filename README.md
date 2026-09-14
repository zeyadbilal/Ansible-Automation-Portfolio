# Ansible Automation Portfolio

This repository contains two practical DevOps automation tasks built with Ansible to demonstrate infrastructure provisioning, configuration management, and Linux service automation. The project combines a web server deployment with a repository manager installation, showing both foundational automation skills and the ability to structure automation using reusable roles.

## Project Purpose

The goal of this project is to showcase hands-on experience with:

- Infrastructure as Code (IaC)
- Ansible playbooks and Jinja2 templates
- Linux administration and service configuration
- Systemd-based service management
- Configuration drift prevention through automation
- Reusable role-based automation design

This portfolio project is suitable for a GitHub repository, resume, or technical interview discussion.

---

## Project 1: NGINX Deployment with Ansible

### Objective

Deploy and configure an NGINX web server on a Linux host using Ansible, while demonstrating both a simple playbook workflow and a role-based modular automation approach.

### What is included

- Installation of NGINX using Ansible
- Configuration of the NGINX service
- Change of the web server port from the default port 80 to port 8080
- Deployment of a custom HTML page using templates
- Host-specific dynamic content using variables or facts
- Use of handlers to restart the service on config changes
- Two approaches:
  - a standard playbook structure
  - a reusable Ansible role structure

### Key configuration features

- Service installed and started automatically
- Custom NGINX configuration managed through templates
- Dynamic web page generation for each target host
- Improved maintainability using role-based design

### Example use case

A system administrator wants to deploy a lightweight web server across multiple Linux machines with a single automated configuration workflow. This project demonstrates how to manage that process consistently and repeatably with Ansible.

---

## Project 2: Sonatype Nexus Repository Manager Deployment

### Objective

Automate the installation and configuration of Sonatype Nexus Repository Manager 3 on a Linux host, with service management and deployment configuration handled by Ansible.

### What is included

- Java installation for Nexus compatibility
- Download and extraction of Nexus binaries
- Creation of a dedicated `nexus` system user and group
- Permission and ownership configuration for Nexus directories
- Configuration to run Nexus as a dedicated service user
- JVM memory and networking settings adjustment
- Service configured to run on port 8081
- Systemd service creation and activation using handlers

### Key configuration features

- Enables startup integration with systemd
- Creates a non-root execution environment for Nexus
- Sets the application to listen on port 8081
- Uses idempotent Ansible tasks for repeatable deployment
- Demonstrates practical service lifecycle automation

### Example use case

This is useful for teams that need a private package repository for Java artifacts, Docker images, or other software packages. The project shows how infrastructure automation can support internal software distribution and artifact management.

---

## Skills Demonstrated

This project highlights a wide range of automation and DevOps skills, including:

- Ansible playbook development
- Ansible roles and modular automation
- YAML configuration syntax
- Jinja2 templating
- Linux service management with systemd
- Secure user and permission setup
- Web server deployment and configuration
- Artifact repository setup and maintenance
- Infrastructure automation for real-world production-like tasks

---

## Repository Structure

```text
ansible-automation-portfolio/
├── README.md
├── ansible_tasks.txt
├── 01-nginx-automation/
│   ├── plain-playbook/
│   │   ├── ansible.cfg
│   │   ├── inventory.ini
│   │   ├── playbook.yml
│   │   ├── nginx.conf.j2
│   │   ├── the_page/
│   │   └── steps/
│   └── role-based/
│       ├── ansible.cfg
│       ├── inventory.ini
│       ├── playbook.yml
│       ├── roles/
│       │   └── role1/
│       └── steps/
├── 02-nexus-automation/
│   ├── ansible.cfg
│   ├── inventory.ini
│   ├── nexus.service.j2
│   ├── playbook.yml
│   └── steps/
└──
```

---

## Technologies Used

- Ansible
- Linux / Ubuntu
- NGINX
- Sonatype Nexus Repository Manager
- Java OpenJDK
- systemd
- Jinja2 templates
- SSH-based remote administration

---

## Prerequisites

To use this project, you should have:

- Ansible installed on the control machine
- SSH access to target Linux hosts
- A configured inventory file for your environment
- Sudo or root privileges on managed hosts
- Basic knowledge of Linux service administration

---

## How to Run

### 1. NGINX project

```bash
cd 01-nginx-automation/plain-playbook
ansible-playbook -i inventory.ini playbook.yml
```

Or with the role-based version:

```bash
cd 01-nginx-automation/role-based
ansible-playbook -i inventory.ini playbook.yml
```

### 2. Nexus project

```bash
cd 02-nexus-automation
ansible-playbook -i inventory.ini playbook.yml
```

---

## CV / Portfolio-Friendly Summary

A short version you can use in a CV or LinkedIn profile:

> Automated deployment and configuration of Linux services using Ansible, including NGINX web server setup and Sonatype Nexus installation. Managed systemd services, templated configuration files, user permissions, and service startup automation to improve consistency and reduce manual operations in infrastructure environments.

---

## Why This Project Is Valuable

This project demonstrates more than simple scripting. It shows that I can:

- automate infrastructure tasks reliably
- write reusable and maintainable automation code
- configure services in realistic Linux environments
- structure playbooks for scale and readability
- apply configuration management concepts in practice

These are core skills for entry-level or junior DevOps, Cloud, System Administrator, and Automation Engineer roles.

---

## Recommended Repository Name

```text
ansible-automation-portfolio
```

---

## License

This project is intended for educational and portfolio purposes.
