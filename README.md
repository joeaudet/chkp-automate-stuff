Various info and examples for Check Point automation  

Check Point Main Github: <https://github.com/CheckPointSW>

Check Point AWS CloudFormation Templates: <https://support.checkpoint.com/results/sk/sk111013>

### Documentation Links:

API Documentation links:  
- Mgmt API (policy / blade management): <https://sc1.checkpoint.com/documents/latest/APIs/index.html>
    - Mgmt API Postman Collections: <https://community.checkpoint.com/t5/API-CLI-Discussion/Postman-Collections-links-to-all-available-and-the-basics/td-p/40923>
- Gaia API (Gateway OS settings): <https://sc1.checkpoint.com/documents/latest/GaiaAPIs/index.html>
    - Gaia API Postman Collection: <https://github.com/CheckPointSW/CloudGuardIaaS/tree/master/common/cme_api_postman>
- CME API: <https://app.swaggerhub.com/apis-docs/Check-Point/cme-api/v1#/>
    - CME API Postman Collection: <https://github.com/CheckPointSW/CloudGuardIaaS/tree/master/common/cme_api_postman>

Cloud Management Extension (CME) admin guide: <https://sc1.checkpoint.com/documents/IaaS/WebAdminGuides/EN/CP_CME/Content/Topics-CME/Overview.htm?tocpath=_____3>

Developer Resources:  
- <https://developer.checkpoint.com/>
- Check Point CloudGuard Network Repository Overview: <https://github.com/CheckPointSW/CloudGuardIaaS>

IAC providers:  
- Ansible:  
    - Getting started with Ansible: <https://support.checkpoint.com/results/sk/sk114661>
    - <https://github.com/CheckPointSW/cpAnsible>
    - <https://docs.ansible.com/ansible/latest/collections/check_point/mgmt/index.html>
- Terraform: <https://registry.terraform.io/providers/CheckPointSW/checkpoint/latest>

Check Point Mgmt API - Python SDK: <https://github.com/CheckPointSW/cp_mgmt_api_python_sdk>

Export/Import Policy Package (requires python SDK): <https://github.com/CheckPointSW/ExportImportPolicyPackage>

Checkmates Codehub (community discussions / examples): <https://community.checkpoint.com/t5/API-CLI-Discussion/bd-p/codehub>

## Dynamically Updatable Components:
- These features need Mgmt and Gateways at version R81.20 or above
    - [External Network Feeds](https://sc1.checkpoint.com/documents/R81.20/WebAdminGuides/EN/CP_R81.20_SecurityManagement_AdminGuide/Content/Topics-SECMG/Network_Feed.htm)
- These features need Mgmt and Gateways at version R82 or above and Need to use GAIA API v1.8
    - [Dynamic Layer in Access Control Policy](https://support.checkpoint.com/results/sk/sk182252) - 