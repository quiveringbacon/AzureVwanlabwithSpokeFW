# Azure Vwan lab with Spoke FW

This creates a vwan with a hub and a couple of spoke vnets with VM's and a firewall vnet all connected to the vhub. All internet traffic is pointed to the Azure firewall in the firewall vnet. You'll be prompted for the resource group name, location where you want the resources created, your public ip and username and password to use for the VM's. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip and route tables are added sending traffic to your public ip to the internet.

The topology will look like this:

![wvanlabwithspokefw](https://user-images.githubusercontent.com/128983862/232794132-32dcb280-b039-4ed7-bb5d-6f4f745d0432.png)

You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureVwanlab.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
