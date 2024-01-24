Login to domain (MDS):

Body:

```
{
  "user" : "username",
  "password" : "password",
  "domain" : "domain_name"
}
```

Successful Result (SID = session ID):

```
{
    "uid": "86546f8f-5b93-4bd3-8fea-3753fb356cd4",
    "sid": "DaDShnhQwrR0KecGXX3Ia7sVPl88eE8M_NXP9A6sknc",
    "url": "https://192.168.50.200:443/web_api",
    "session-timeout": 600,
    "last-login-was-at": {
        "posix": 1700604432191,
        "iso-8601": "2023-11-21T17:07-0500"
    },
    "api-server-version": "1.9",
    "user-name": "admin",
    "user-uid": "9c2d6e83-533e-4e27-bbe0-7f905a5ed5cb"
}
```

To get list of domain names, login to system domain:  
```
{
  "user" : "username",
  "password" : "password",
  "domain" : "domain_name"
}
```

API call: show-domains
```
{
  "limit" : 50,
  "offset" : 0,
  "details-level" : "standard"
}
```

Successful result:

```
{
    "objects": [
        {
            "uid": "e8672b54-8c0f-4720-9f79-a8f2e4280712",
            "name": "DOMAIN1",
            "type": "domain",
            "domain": {
                "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
                "name": "System Data",
                "domain-type": "mds"
            },
            "icon": "Objects/domain",
            "color": "black"
        },
        {
            "uid": "d46d5c43-ebd9-409b-acc7-46a7b2beebf6",
            "name": "DOMAIN2",
            "type": "domain",
            "domain": {
                "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
                "name": "System Data",
                "domain-type": "mds"
            },
            "icon": "Objects/domain",
            "color": "black"
        },
        {
            "uid": "4ee9c8dd-7865-400d-be65-2c853b12a6a5",
            "name": "DOMAIN3",
            "type": "domain",
            "domain": {
                "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
                "name": "System Data",
                "domain-type": "mds"
            },
            "icon": "Objects/domain",
            "color": "black"
        }
    ],
    "from": 1,
    "to": 3,
    "total": 3
}
```