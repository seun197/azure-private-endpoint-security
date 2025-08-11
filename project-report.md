# Azure Private Endpoints Implementation – Detailed Report

## Objective
Secure Azure Storage by eliminating public access and enforcing private network access via Azure Private Endpoints, aligned with ISO 27001 compliance requirements.

## Risk Addressed
Publicly exposed Azure Storage endpoints could allow unauthorized access or data exfiltration, compromising FSCS claimant data confidentiality and integrity.

## Implementation Steps
1. **Create Storage Account**  
   - Provisioned `fscsstorage` in Azure.

2. **Disable Public Network Access**  
   - Networking > Public network access → Set to `Disabled`.

3. **Configure Private Endpoint**  
   - Added a Private Endpoint linked to `privatenet` (FSCS-like VNet).  
   - Integrated with the appropriate subnet.

4. **DNS Verification**  
   - From VM inside VNet:  
     - `nslookup fscsstorage.blob.core.windows.net` → resolved to `10.1.0.5` (private IP via privatelink).  
   - From personal laptop outside VNet:  
     - Resolved to public IP; access blocked.

5. **Access Testing**  
   - Internal VM: Full access to blob storage.  
   - External device: Denied.

## Compliance Mapping
- **ISO 27001 A.13.1** – Network Security Management  
- **ISO 27001 A.9.1** – Access Control Policy

## Outcome
- Public attack surface for Azure Storage eliminated.
- All traffic contained within Azure backbone via Private Link.
- Reduced risk of data exfiltration while maintaining legitimate internal access.

## Supporting Files
- [Secure Azure Storage Access via Private Endpoint.txt](Secure%20Azure%20Storage%20Access%20via%20Private%20Endpoint.txt)
- Screenshots in `/images` directory.
