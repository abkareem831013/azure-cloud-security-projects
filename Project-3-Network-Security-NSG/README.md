# Azure Network Security using Network Security Groups (NSG)

## Objective
Implement network-level security in Azure by configuring Network Security Groups (NSGs) to control inbound traffic and restrict unauthorized access to resources.

## Tools & Services Used
- Azure Virtual Network (VNet)
- Network Security Groups (NSG)
- Azure Subnets

## Architecture
Internet → NSG → Subnet → Azure Resources

## Implementation Steps
1. Created a secure Azure Virtual Network with dedicated subnet
2. Created a Network Security Group (NSG)
3. Configured inbound security rules to allow access only from trusted IP
4. Associated NSG with subnet to enforce traffic filtering

## Security Best Practices Applied
- Least privilege network access
- Restricted inbound traffic
- Default deny rules
- Network segmentation

## Outcome
Successfully secured Azure network resources by enforcing strict inbound access controls using Network Security Groups.
