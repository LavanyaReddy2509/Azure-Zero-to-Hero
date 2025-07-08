# Azure Networking

**Azure Virtual Network (VNet)** is a logical isolation of the Azure cloud dedicated to your subscription. It allows Azure resources (like VMs, databases, etc.) to securely communicate with each other, the internet, and on-premises networks.

A Virtual Network (VNet) in Azure is a logically isolated network that securely connects Azure resources and extends on-premises networks. Key features include:

- **Isolation**: VNets provide isolation at the network level for segmenting resources and controlling traffic.

- **Subnetting**: Divide a VNet into subnets for resource organization and traffic control.

- **Address Space**: VNets have an address space defined using CIDR notation, determining the IP address range.

**🔧 Key Features of Azure VNet:**
| **Feature**  |	**Description** |
|:-----------|:------------:|
| Subnets	| Divide your VNet into smaller networks to isolate workloads. |
| Network Security Groups (NSG) |	Control inbound/outbound traffic to/from resources. |
| VNet Peering	| Connect VNets across regions or subscriptions. |
| VPN Gateway / ExpressRoute |	Connect on-premises networks to Azure VNet. |
| Private Endpoints |	Access Azure services over a private IP. |
| Service Endpoints	| Extend your VNet to Azure services (like Blob Storage). |
| DNS  | Support	Use Azure-provided DNS or custom DNS servers. |
## Subnets, CIDR

### Subnets

Subnets are subdivisions of a Virtual Network, allowing for better organization and traffic management.

### CIDR (Classless Inter-Domain Routing)

CIDR notation represents IP addresses and their routing prefix, specifying the range of IP addresses for a network.

## Routes and Route Tables

### Routes

Routes dictate how network traffic is directed, specifying the destination and next hop.

### Route Tables

Route Tables are collections of routes associated with subnets, enabling custom routing rules.

## Network Security Groups (NSGs)

NSGs are fundamental for Azure's network security, allowing filtering of inbound and outbound traffic. Key aspects include:

- **Rules**: NSGs define allowed or denied traffic based on source, destination, port, and protocol.

- **Default Rules**: NSGs have default rules for controlling traffic within the Virtual Network and between subnets.

- **Association**: NSGs can be associated with subnets or individual network interfaces.

## Application Security Groups (ASGs)

ASGs group Azure virtual machines based on application requirements, simplifying network security:

- **Simplification**: ASGs allow defining rules based on application roles instead of individual IP addresses.

- **Dynamic Membership**: ASGs support dynamic membership based on tags or other attributes.

- **Rule Association**: Security rules can be associated with ASGs for intuitive and scalable network security management.
