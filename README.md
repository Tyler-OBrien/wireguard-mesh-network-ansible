Based off: https://jawher.me/wireguard-ansible-systemd-ubuntu/

This aims to automate the deployment of a mesh network using wireguard.

This uses wg-quick, and sets up UFW as well.

# Usage

Configure your inventory.yml (Set up hosts, wireguard port, if UFW will be used, etc)

ansible-playbook -i "inventory.yml" "wireguard.yml"

After setting it up, try running the ping playbook to verify connectivity

ansible-playbook -i "inventory.yml" "ping.yml"