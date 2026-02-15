# aws-secure-vpc-architecture
Secure AWS VPC with public/private subnets, bastion host, and NAT Gateway.
# Secure AWS VPC Architecture with Bastion Host and NAT Gateway

## Project Overview
This project demonstrates a secure AWS networking architecture using a custom VPC with public and private subnets.
A bastion host is deployed in the public subnet to control SSH access, while application servers run in private subnets
with no public IP addresses. Outbound internet access for private instances is provided through a NAT Gateway.

## Architecture
- Custom VPC (10.0.0.0/16)
- 2 Public Subnets
- 2 Private Subnets
- Internet Gateway for public access
- NAT Gateway for outbound internet access from private subnets
- Bastion Host in public subnet
- Private EC2 instance without public IP

## AWS Services Used
- Amazon VPC
- Amazon EC2
- NAT Gateway
- Internet Gateway
- Security Groups
- Route Tables

## Security Design
- SSH access allowed only to the bastion host from a trusted IP
- Private EC2 instances allow SSH only from the bastion host
- No public IPs assigned to private instances

## Validation
Outbound internet access from private EC2 was validated using:
```bash
curl google.com

## Outcome

- Successfully implemented a secure AWS VPC architecture with public and private subnets.
- Designed controlled SSH access using a bastion host.
- Ensured private EC2 instances had no public IP exposure.
- Enabled outbound-only internet connectivity through a NAT Gateway.
- Validated architecture by testing internet access from private EC2 without direct public access.



