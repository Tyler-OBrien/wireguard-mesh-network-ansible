Based off: https://jawher.me/wireguard-ansible-systemd-ubuntu/

This aims to automate the deployment of a mesh network using wireguard.

This uses wg-quick, and sets up UFW as well.

# Usage

This is intended to be use to create a wireguard mesh network, securing communication and essentially creating a private VLAN between various servers. I used it to create a mesh network of 8 different Virtual Private Servers from 3 different providers. If you are behind NAT or a stateful firewall, you might need to set PersistentKeepalive.

Configure your inventory.yml (Set up hosts, wireguard port, if UFW will be used, etc)

ansible-playbook -i "inventory.yml" "wireguard.yml"

After setting it up, try running the ping playbook to verify connectivity

ansible-playbook -i "inventory.yml" "ping.yml"
