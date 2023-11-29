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