Firewall
========

Firewall whitelist using IPTables

Requirements
------------

None

Role Variables
--------------

Defaults:  
- **ssh_in**:                   true
- **ssh_out**:                  false
- **http_in**:                  false
- **http_out**:                 true
- **https_in**:                 false
- **https_out**:                true
- **git_out**:                  false
- **git_port**:                 9418
- **papertrail_out**:           true
- **mongodb_in**:               false
- **mongodb_out**:              false
- **mongodb_port**:             27017
- **redis_in**:                 false
- **redis_out**:                false
- **rabbitmq_in**:              false
- **rabbitmq_out**:             false
- **rabbitmq_port**:            5672
- **rabbitmq_management**:      false
- **rabbitmq_management_ip**:   127.0.0.1
- **rabbitmq_management_port**: 15672


Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - role: ryanlelek.firewall
           http_in: true
           https_in: true

License
-------

MIT

Author Information
------------------

Created by [Ryan Lelek](https://www.ryanlelek.com)  
Part of [AnsibleTutorials.com](http://www.ansibletutorials.com)
