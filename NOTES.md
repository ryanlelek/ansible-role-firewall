
Additional Notes
================

# IPTables Configuration Template

```
# Host Group Loop
# {% for host in groups['rabbitmq_access'] %}
#   CODE
# {% endfor %}

# Host Restrictions
# -s {{ hostvars[host]['ansible_eth1']['ipv4']['address'] }}
# -d {{ hostvars[host]['ansible_eth1']['ipv4']['address'] }}

```
