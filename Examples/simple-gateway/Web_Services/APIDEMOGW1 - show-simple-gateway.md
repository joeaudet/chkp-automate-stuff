###API call: show-simple-gateway

Body:
```
{
  "name" : "APIDEMOGW1"
}
```

Successful results:
```
{
    "uid": "9f1072de-62d8-44d4-bb23-923516a123bc",
    "name": "APIDEMOGW1",
    "type": "simple-gateway",
    "domain": {
        "uid": "d46d5c43-ebd9-409b-acc7-46a7b2beebf6",
        "name": "DOMAIN2",
        "domain-type": "domain"
    },
    "interfaces": [
        {
            "uid": "eb4ce20e-de5a-45e1-8418-562119e856f8",
            "name": "eth0",
            "network-interface-type": "ethernet",
            "ipv4-address": "192.168.14.184",
            "ipv4-network-mask": "255.255.255.0",
            "ipv4-mask-length": 24,
            "ipv6-address": "",
            "comments": "",
            "color": "black",
            "icon": "NetworkObjects/network",
            "topology": "external",
            "anti-spoofing": true,
            "anti-spoofing-settings": {
                "action": "prevent",
                "exclude-packets": false,
                "spoof-tracking": "log"
            },
            "security-zone": false
        },
        {
            "uid": "879c4157-b279-4896-bde7-db19a841c1be",
            "name": "eth1",
            "network-interface-type": "ethernet",
            "ipv4-address": "192.168.80.184",
            "ipv4-network-mask": "255.255.255.0",
            "ipv4-mask-length": 24,
            "ipv6-address": "",
            "comments": "",
            "color": "black",
            "icon": "NetworkObjects/network",
            "topology": "internal",
            "topology-settings": {
                "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
                "interface-leads-to-dmz": false
            },
            "anti-spoofing": true,
            "anti-spoofing-settings": {
                "action": "prevent",
                "exclude-packets": false,
                "spoof-tracking": "log"
            },
            "security-zone": false
        }
    ],
    "ipv4-address": "192.168.14.184",
    "dynamic-ip": false,
    "version": "R81.20",
    "os-name": "Gaia",
    "hardware": "Open server",
    "sic-name": "CN=APIDEMOGW1,O=DOMAIN2_Server.lab.joeaudet.com.4ay2c4",
    "sic-state": "communicating",
    "firewall": true,
    "firewall-settings": {
        "auto-maximum-limit-for-concurrent-connections": true,
        "maximum-limit-for-concurrent-connections": 25000,
        "auto-calculate-connections-hash-table-size-and-memory-pool": true,
        "connections-hash-size": 131072,
        "memory-pool-size": 6,
        "maximum-memory-pool-size": 30
    },
    "vpn": true,
    "vpn-settings": {
        "useClientlessVpn": false,
        "maximum-concurrent-ike-negotiations": 1000,
        "maximum-concurrent-tunnels": 10000,
        "vpn-domain-type": "addresses_behind_gw",
        "vpn-domain-exclude-external-ip-addresses": false,
        "link-selection": {
            "ip-selection": "use-main-address"
        },
        "remote-access": {
            "support-l2tp": false,
            "allow-vpn-clients-to-route-traffic": false,
            "support-nat-traversal-mechanism": true,
            "nat-traversal-service": {
                "uid": "97aeb390-9aea-11d5-bd16-0090272ccb30",
                "name": "VPN1_IPSEC_encapsulation",
                "type": "service-udp",
                "domain": {
                    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                    "name": "Check Point Data",
                    "domain-type": "data domain"
                },
                "port": "2746",
                "icon": "Services/UDPService",
                "color": "firebrick"
            },
            "support-visitor-mode": true,
            "visitor-mode-service": {
                "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30",
                "name": "https",
                "type": "service-tcp",
                "domain": {
                    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                    "name": "Check Point Data",
                    "domain-type": "data domain"
                },
                "port": "443",
                "icon": "Protocols/HTTP",
                "color": "red"
            },
            "visitor-mode-interface": "All IPs"
        },
        "office-mode": {
            "mode": "off"
        },
        "authentication": {}
    },
    "application-control": true,
    "url-filtering": true,
    "threat-prevention-mode": "custom",
    "ips": true,
    "threat-emulation": true,
    "threat-extraction": false,
    "data-loss-prevention": false,
    "qos": false,
    "anti-bot": true,
    "anti-virus": true,
    "content-awareness": false,
    "zero-phishing": false,
    "save-logs-locally": false,
    "send-alerts-to-server": [
        "DOMAIN2_Server"
    ],
    "send-logs-to-server": [
        "DOMAIN2_Server"
    ],
    "send-logs-to-backup-server": [],
    "logs-settings": {
        "rotate-log-by-file-size": false,
        "rotate-log-file-size-threshold": 1000,
        "rotate-log-on-schedule": false,
        "alert-when-free-disk-space-below-metrics": "mbytes",
        "alert-when-free-disk-space-below": true,
        "alert-when-free-disk-space-below-threshold": 20,
        "alert-when-free-disk-space-below-type": "popup alert",
        "delete-when-free-disk-space-below-metrics": "mbytes",
        "delete-when-free-disk-space-below": true,
        "delete-when-free-disk-space-below-threshold": 5000,
        "before-delete-keep-logs-from-the-last-days": false,
        "before-delete-keep-logs-from-the-last-days-threshold": 3664,
        "before-delete-run-script": false,
        "before-delete-run-script-command": "",
        "stop-logging-when-free-disk-space-below-metrics": "mbytes",
        "stop-logging-when-free-disk-space-below": true,
        "stop-logging-when-free-disk-space-below-threshold": 100,
        "reject-connections-when-free-disk-space-below-threshold": false,
        "reserve-for-packet-capture-metrics": "mbytes",
        "reserve-for-packet-capture-threshold": 500,
        "delete-index-files-when-index-size-above-metrics": "mbytes",
        "delete-index-files-when-index-size-above": false,
        "delete-index-files-when-index-size-above-threshold": 100000,
        "delete-index-files-older-than-days": false,
        "delete-index-files-older-than-days-threshold": 14,
        "forward-logs-to-log-server": false,
        "perform-log-rotate-before-log-forwarding": false,
        "update-account-log-every": 3600,
        "detect-new-citrix-ica-application-names": false,
        "turn-on-qos-logging": true,
        "distribute-logs-between-all-active-servers": false
    },
    "identity-awareness": false,
    "platform-portal-settings": {
        "enabled": true,
        "portal-web-settings": {
            "main-url": "https://192.168.14.184/",
            "ip-address": "192.168.14.184",
            "aliases": []
        },
        "accessibility": {
            "allow-access-from": "RULE_BASE"
        }
    },
    "usercheck-portal-settings": {
        "enabled": true,
        "portal-web-settings": {
            "main-url": "http://192.168.14.184/UserCheck",
            "ip-address": "192.168.14.184",
            "aliases": []
        },
        "accessibility": {
            "allow-access-from": "INTERNAL_INTERFACES",
            "internal-access-settings": {
                "undefined": false,
                "dmz": false,
                "vpn": true
            }
        }
    },
    "proxy-settings": {
        "use-custom-proxy": false
    },
    "nat-hide-internal-interfaces": true,
    "nat-settings": {
        "auto-rule": false
    },
    "fetch-policy": [
        "DOMAIN2_Server"
    ],
    "hit-count": true,
    "enable-https-inspection": false,
    "application-control-and-url-filtering-settings": {
        "global-settings-mode": "use_global_settings"
    },
    "https-inspection": {
        "bypass-on-failure": {
            "override-profile": false,
            "profile-value": true
        },
        "site-categorization-allow-mode": {
            "override-profile": false,
            "profile-value": "hold"
        },
        "deny-untrusted-server-cert": {
            "override-profile": false,
            "profile-value": false
        },
        "deny-revoked-server-cert": {
            "override-profile": false,
            "profile-value": true
        },
        "deny-expired-server-cert": {
            "override-profile": false,
            "profile-value": false
        }
    },
    "ips-update-policy": "gateway automatic update",
    "groups": [],
    "comments": "",
    "color": "yellow",
    "icon": "NetworkObjects/gateway",
    "tags": [],
    "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
            "posix": 1700603130142,
            "iso-8601": "2023-11-21T16:45-0500"
        },
        "last-modifier": "admin",
        "creation-time": {
            "posix": 1700602104647,
            "iso-8601": "2023-11-21T16:28-0500"
        },
        "creator": "admin"
    },
    "read-only": false,
    "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "not_supported"
    }
}
```