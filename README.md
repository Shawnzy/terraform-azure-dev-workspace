# Azure Remote Development Workspace Setup with Terraform

This repository contains Terraform configurations for setting up a complete remote development workspace in Microsoft Azure. It automates the provisioning of a virtual network, subnets, security groups and rules, network interfaces, and a virtual machine suitable for development purposes.

## Project Overview
The goal of this project is to provide an easy and repeatable way to deploy a development environment in Azure using Infrastructure as Code (IaC) practices with Terraform.

### Prerequisites
- Azure Account
- Terraform installed on your local machine
- Basic understanding of Azure services and Terraform

### Azure Resources Created
- **Provider**: Azure Provider configured for Terraform.
- **Resource Group**: A container that holds related resources for an Azure solution.
- **Virtual Network (VNet)**: The network for all Azure services in your setup.
- **Subnets**: Subdivisions within the VNet.
- **Security Groups and Rules**: Sets of rules to allow or deny network traffic to your resources.
- **Network Interface (NIC)**: Connects Azure VMs to the intended VNet.
- **Virtual Machine (VM)**: Azure VM set up for development work.

### Customization
Variables can be customized in the `variables.tf` file, including:

- **Host OS**: Operating system for the VM.
- **Environment**: Designation for the deployment environment (e.g., dev, test, prod).
- **Source IP Address**: IP address ranges allowed to access the resources.
- **Region**: Azure region for deploying the resources.

## Getting Started

### Configuration
Clone the repository:

```bash
git clone https://github.com/Shawnzy/terraform-azure-dev-workspace.git
cd terraform-azure-dev-workspace
```

### Setting up Azure Credentials
Ensure that your Azure credentials are configured properly. You can set them up using Azure CLI or by setting environment variables.

### Terraform Initialization
Initialize Terraform to download the necessary providers:
```bash
terraform init
```  

### Planning
Review the Terraform execution plan to see the actions Terraform will perform:
```bash
terraform plan
```

### Applying
Apply the configuration to start building the AWS infrastructure:
```bash
terraform apply -auto-approve
```

### Cleaning Up (local Terraform directory)
To remove the AWS infrastructure, use:
```bash
terraform destroy
```

### Disclaimer
This project is for demonstration purposes and not meant for production use without proper modifications and security considerations.
 
