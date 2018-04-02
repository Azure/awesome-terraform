Terraform deployment of VM Scale Set
===

This folder has the complete code presented in the [Terraform for VMSS codelab](https://docs.microsoft.com/en-us/azure/terraform/terraform-create-vm-scaleset-network-disks-hcl).


This codelab deploys the following resources to your Azure subscription:

* A virtual network with the CIDR 10.0.0.0/16
* Two public IP addresses
* An Azure load balancer
* A virtual machine scale set attached to the vnet
* A virtual machine connected to the vnet

Deploy the resources with the following steps:

* [Install Terraform and configure access to Azure](/azure/virtual-machines/linux/terraform-install-configure)
* Clone or copy this directory 
* Run the following commands

```bash
terraform init
terraform plan
terraform apply
```

You will be asked to enter the password of administrator and the location where you want the resources to be deployed. 

The last command outputs the FQDN of the loadbalancer that exposes the NGINX deployed on the scaleset and the FQDN of the VM that used as a jumpbox to access each node of the VM Scale Set.
