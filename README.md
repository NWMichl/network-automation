# network-automation

Collection of ansible playbooks and little InfraAsCode nuggets

### nxos_desc.yml: Search for an interface description

If you are documenting names of endhosts or servers using the interface description and have no easy way to fetch this information in some form of central config management tool, this one is for you!
The playbook prompts for the search string and loops over all devices in "hostgroup".

Use 

```
ansible-playbook -k nxos_desc.yml --limit <hostgroup>
```

to log into the hosts with the local linux user (SSH password prompt).

Tested with ansible 2.5.3 on RHEL7 and Cisco Nexus 9300/9500, but works with Catalyst (6500 VSS, 3560, 2960, ...) as well.
