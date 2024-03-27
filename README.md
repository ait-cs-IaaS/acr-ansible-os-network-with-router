# Ansible-Role: acr-ansible-os-network-with-router

AIT-CyberRange: Creates an openstack network including a distinct router. 


## Requirements

- Debian or Ubuntu
- Openstack

## Role Variables

```yaml
# NETWORK
os_network_name: networkname
os_network_subnet: '{{ os_network_name }}-subnet'
os_network_cidr: 192.168.1.0/24
os_network_dns_nameservers: [8.8.8.8]

# ROUTER
os_router_name: '{{ os_network_name }}-router'
os_router_network: '{{ os_external_network }}'

```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - role: acr-ansible-os-network-with-router
      vars:
        os_network_name: networkname
```

## License

GPL-3.0

## Author

- Tobias Pfaller
- Lenhard Reuter