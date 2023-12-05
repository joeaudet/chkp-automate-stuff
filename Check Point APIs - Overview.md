Check Point API Management call sequence:
- Login
  - (If MDS, specify which domain, otherwise end up in System Data)
  - Capture session ID which is used for all subsequent API calls - will timeout if no activity before timeout period set on Mgmt server
- Run various calls
  - Headers:
    - Content-Type : application/json
    - X-chkp-sid : sid from login (string)
- Some commands will return a task-id: Run `show-task task-id` API call to get output from task
- If anything created or changed, publish
- Logout

Anything not an appliance OS setting is done through [Mgmt API](https://sc1.checkpoint.com/documents/latest/APIs/index.html)  
OS Settings are done through [Gaia API](https://sc1.checkpoint.com/documents/latest/GaiaAPIs/index.html) directly to security appliance

### Important notes

The API is limited to return a max of 500 objects. If you have more than that, you need to iterate through them. The total object count is listed in the bottom of the output object on various show calls (total):
```
    "from": 1,
    "to": 3,
    "total": 3
```
