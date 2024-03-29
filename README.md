# my-playbook

Ansible playbook for deploying my applications

```
# install roles
ansible-galaxy install -r requirements.yml

# dev
ansible-playbook site.yml -i inventory.dev

# prod
ansible-playbook site.yml -i inventory.dev
```

## Example Configuration and Required Variables

```
ansible_connection: ssh
ansible_user: isaac
ansible_ssh_pass: ---

user_name: isaac
real_name: Isaac Lo
nick_name: isaaclo123

domain: isaaclo.site
email: isaaclo123@gmail.com

# external ports
ssh_port: 22
znc_irc_port: 6697
syncthing_listen_port: 22000
http_port: 80
https_port: 443
openvpn_server_port: 1194

# internal ports
syncthing_web_port: 8384
znc_web_port: 8080
bitlbee_server_port: 6667 # this config port is broken and will only work on 6667
radicale_port: 5232

# openvpn
openvpn_client_list:
- client1
- client2
openvpn_credential_path: "~/client_credentials/"

znc_password: ---
radicale_password: ---
syncthing_password: ---
bitlbee_password: ---
openvpn_password: ---
```
