# azure-private-endpoint-security
Implementation of Azure Storage Private Endpoints to eliminate public access and secure claimant data.

# Azure Private Endpoints Implementation

## Overview
This project demonstrates securing Azure Storage access by eliminating public exposure and enforcing private network access via Azure Private Endpoints.

## Risk Addressed
Publicly exposed Azure Storage endpoints could allow unauthorized data access or exfiltration.

## Implementation Steps
1. Created Azure Storage Account.
2. Disabled public network access.
3. Configured Private Endpoint in FSCS-like VNet.
4. Verified DNS resolution to private IP inside VNet.
5. Confirmed public access blocked.

## Validation
- **Private Network (VM in VNet)**: `nslookup` resolved to `10.1.0.5` (private IP).
- **Public Network (personal laptop)**: Resolved to public IP; access blocked.

## Compliance Mapping
- ISO 27001 A.13.1 – Network Security Management
- ISO 27001 A.9.1 – Access Control Policy

## Outcome
✅ Eliminated public attack surface  
✅ All traffic stays within Azure backbone  
✅ Maintained compliance without disrupting internal access

## Screenshots
![Private DNS Test](images/dns-test-private.png)
![Public DNS Test](images/dns-test-public.png)
![Azure Networking](images/azure-networking.png)
![Private Endpoint Config](images/private-endpoint.png)
