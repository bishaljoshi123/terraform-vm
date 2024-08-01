# Terraform For creating VM in google cloud

# Introduction

This is a Virtual Machine IaC (Infrastructure as Code). By applying this Terraform code, the following changes will be made:

1. A service account named vm-manager will be created. This account will be responsible for creating the VM for security purposes.
2. The VM will be created with a firewall policy that allows HTTP, HTTPS, and opens port 9001.
3. Immediately after the VM is created, a startup script will run to install Docker on the VM.

# Steps

Follow following steps to create a vm in google cloud.

1. Download the .json credentials file from your google cloud service account. The account should have the following permissions:

```
Compute Engine Service Agent
Compute Instance Admin (beta)
Compute Network Admin
Compute Organization Firewall Policy Admin
Compute Organization Firewall Policy User
Compute Security Admin
Firebase Rules Admin
Firewall Recommender Admin
Security Admin
Service Account Admin
```

2. Paste the .json credentials file to the root folder of your directory
3. run the following commands

```bash
terraform init # to initialize terraform
terraform plan # to see the changes in GCP
terraform apply # to make changes in GCP
```

Note: to delete the VM run the following command

```bash
terraform destroy
```
