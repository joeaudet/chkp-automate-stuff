Steps to provision a simple gateway:

## Deploy gateway
- Physical gateway
    - [ ] Gateway connected, and powered on
    - [ ] IP used for mgmt assigned to interface
    - [ ] Mgmt Server able to reach gateway (routing needs to be setup)
    - [ ] First Time Wizard (FTW) completed - CLISH, expert, or [Gaia API](https://sc1.checkpoint.com/documents/latest/GaiaAPIs/index.html)
    - [ ] One Time Password - Used by Mgmt Server for establishing SIC (specified when running FTW)
- Cloud Guard Network Gateway
    - [ ] Virtual gateway deployed through cloud provider marketplace, or through some other automation - with FTW completed and OTP SIC key setup
    - [ ] IP used for mgmt assigned to interface
    - [ ] Mgmt Server able to reach gateway (routing needs to be setup)
    - [ ] One Time Password - Used by Mgmt Server for establishing SIC (specified when running FTW)

## Add gateway to management

- [CP Mgmt API](https://sc1.checkpoint.com/documents/latest/APIs/index.html)
    - [Add a gateway using the internal interface subnet and mask topology](/examples/simple-gateway/web-services/add-simple-gateway_with_interface_subnet_and_mask_topology_example.md)
    - [Add a gateway with a specific network group topology](/examples/simple-gateway/web-services/add-simple-gateway_with_network-group_topology_example.md)