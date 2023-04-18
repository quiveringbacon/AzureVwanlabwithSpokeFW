# Azure Vwan lab with Spoke FW

This creates a vwan with a hub and a couple of spoke vnets with VM's and a firewall vnet all connected to the vhub. All internet traffic is pointed to the Azure firewall in the firewall vnet. You'll be prompted for the resource group name, location where you want the resources created, your public ip and username and password to use for the VM's. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip and route tables are added sending traffic to your public ip to the internet.

The topology will look like this:

![wvanlabwithspokefw](https://user-images.githubusercontent.com/128983862/232792914-9fdafd33-b7c5-450e-af79-d93b323460cb.png)

You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureVwanlab.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
