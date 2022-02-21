# Virtual Network

- Isolated network on the cloud
- Has an IP address range
- IP address is a numerical label that helps locate a machine
- Yung private IP, helps to identify the VM (or resource) inside the virtual network
- Subnet is a _subset_ of the IP address range of the vnet.
- All traffic from a VM goes through the **network interface**
- NSGs are assigned either at the network interface level or the subnet level

# Creating a vNet

- By default, creates a 10.1.0.0/16 address space (pero pwede naman ibahin)
- Gagawa din ng default subnet
- Hindi pwede maglipat ng VM to another vnet.
- Pwedeng magkaiba yung RG ng VM and vnet

# Network Security Groups

- Filter inbound and outbound traffic from your resources
- There are default rules
  - Allow traffic within the virtual network
  - Allow traffic from an Azure load balancer
  - Deny all other traffic
- Attached to the network interface, which is attached to the VM

# Application Security Groups

- Instead of using IP address, pwede mo ilagay yung VM sa ASG, then yung ASG yung gagamitin ng NSG.

# Network Connectivity Options

## Virtual Network Peering

- Used to connect virtual networks together
- Pwede rin gamitin yung peering to connect two networks na magkaiba yung subscription (RDsec + TrendPH IT Ops)

## Point-To-Site VPN connection

- Used for multiple clients accessing Azure resources via private IP
- Use VPN gateway
  - Uses certificates to make it secure

## Site-To-Site VPN connection

- Parang yung ginagawa sa Trend
- Used for entire data centers
- Data center -> Routing device -> VPN gateway/Local network gateway

# Azure ExpressRoute

- All traffic flows through the Microsoft Backbone network
- Provides direct connectivity to Azure services
