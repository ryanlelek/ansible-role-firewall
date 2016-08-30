Firewall
========

Firewall whitelist using IPTables

Requirements
------------

None

Role Variables
--------------

Defaults:  
```
---
tcp_in:
  - 22
tcp_out:
  - 22
  - 80
  - 443
udp_in:
udp_out:
restricted:
```

Dependencies
------------

None

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: ryanlelek.firewall
      tcp_in:
        - 80
        - 443
      tcp_out:
        - 22
        - 80
        - 443
        # Git
        - 9418
      udp_in:
      udp_out:
        # Syslog / Papertrail
        - 32507
      restricted:
        - protocol: tcp
          port: 22
          ip: [YOUR IP ADDRESS OR RANGE HERE]
```

License
-------

MIT

Author Information
------------------

Created by [Ryan Lelek](https://www.ryanlelek.com)  
Part of [AnsibleTutorials.com](http://www.ansibletutorials.com)
