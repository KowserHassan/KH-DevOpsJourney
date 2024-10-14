## Introduction to Terraform 

Terraform is an open-source infrastructure-as-code (IaC) tool created by HashiCorp. 

- cloud agnostic tool - it can deploy code to any cloud provider through terraform registry 

It allows you to:
- define
- provide
- and manage infrastructure using a declarative configuration language.

This means instead of manually setting up cloud resources like servers, databases, and networking, you write code in Terraform to automate these tasks.

## Infra Orchestration vs Config Management

- two key concepts in managing IT environments but they serve different purposes

| **Category**               | **Infrastructure Orchestration**                                      | **Configuration Management**                                        |
|----------------------------|-----------------------------------------------------------------------|---------------------------------------------------------------------|
| **Focus**                  | Automating the provisioning and management of entire infrastructure.  | Managing the specific settings and state of systems post-provision. |
| **Goal**                   | Coordinates cloud resources (servers, networks, etc.).                | Ensures systems remain in the desired state over time.              |
| **Example Tools**          | Terraform, AWS CloudFormation.                                        | Ansible, Chef, Puppet.                                              |
| **Key Actions**            | Provisions infrastructure and manages dependencies.                   | Installs and configures software, enforces system settings.         |
| **Use Case**               | Automating setup of cloud environments with servers, databases, etc.  | Ensuring software/configuration consistency across servers.         |

