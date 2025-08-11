# ISO 27001 Control A.9.1 – Access Control Policy

## Control Requirement
Limit access to information and systems based on business and security requirements.

## How This Project Meets the Control
- Restricted Azure Storage account access to private VNet only.
- Enforced authentication and authorization via Azure AD and role assignments.
- Eliminated all anonymous/public access vectors.

## Evidence
- Azure portal "Public Network Access: Disabled" screenshot.
- Access denied test from non-VNet environment.
- Private endpoint configuration details.
