Check Point API Management call sequence:
1. Login
  - (If MDS, specify which domain, otherwise end up in System Data)
  - Capture session ID which is used for all subsequent API calls - will timeout if no activity before timeout period set on Mgmt server
1. Run various calls
  - Headers:
    - Content-Type : application/json
    - X-chkp-sid : sid from login (string)
1. If anything created or changed, publish
1. Logout

Anything not an appliance OS setting is done through [Mgmt API](https://sc1.checkpoint.com/documents/latest/APIs/index.html)
OS Settings are done through [Gaia API](https://sc1.checkpoint.com/documents/latest/GaiaAPIs/index.html) directly to security appliance


