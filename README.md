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
<img width="955" height="917" alt="01 Storage Acc  Public Net" src="https://github.com/user-attachments/assets/82427265-1199-49cc-85ff-9c817131f2b1" />
<img width="959" height="749" alt="02 Private Netw" src="https://github.com/user-attachments/assets/e441c436-5340-4ea3-ba9e-0c763a0fbde4" />
<img width="841" height="513" alt="03 Vmac in same Vnet as private Vnet" src="https://github.com/user-attachments/assets/2e9caf1a-5933-4b55-9d19-f7a28465e299" />
<img width="767" height="574" alt="04 My Personal laptop conencting to private IP" src="https://github.com/user-attachments/assets/2af51ed5-77f0-4248-b43f-02496aa3a5e6" />
