# Ansible VPN server setup

## Setup server

```shell
ansible-playbook -i ubuntu-16.04LTS/vpn_hosts ubuntu-16.04LTS/vpn.yml
```

## Configure clients

For IKEv2 clients config refer https://gist.github.com/karlvr/34f46e1723a2118bb16190c22dbed1cc#client-setup

To be able to use `On demand` switcher on iOS client create profile (use Apple Configurator and refer to [example](examples/IKEv2-VPN-profile.mobileconfig)) and add following lines:
```xml
<key>OnDemandEnabled</key>
<integer>1</integer>
<key>OnDemandRules</key>
<array>
  <dict>
    <key>Action</key>
    <string>Connect</string>
  </dict>
</array>
```
