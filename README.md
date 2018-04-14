# Ansible VPN server setup

## Setup server

```shell
ansible-playbook -i ubuntu-16.04LTS/vpn_hosts ubuntu-16.04LTS/vpn.yml
```

## Configure clients

For IPSec clients config refer https://gist.github.com/karlvr/34f46e1723a2118bb16190c22dbed1cc#client-setup
