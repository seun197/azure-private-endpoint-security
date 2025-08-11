# ISO 27001 Control A.13.1 – Network Security Management

## Control Requirement
Establish and manage network controls to protect information in networks and supporting information processing facilities.

## How This Project Meets the Control
- Implemented Azure Private Endpoints for storage access.
- Disabled public network access, enforcing traffic routing through secure Azure backbone.
- Configured DNS resolution to private IP addresses inside VNet.
- Blocked public internet traffic to sensitive data storage.

## Evidence
- DNS test results (see `/images`).
- Azure portal configuration screenshots.
- Access denied test from external network.
