## How to install wireguard

The inventory is on the way ```./inventories/prod/hosts``` . Change the IP address, name of the VM and ```ansible_ssh_pass```.

Change the variable ```docker_users``` (default 'user')  ```./inventories/prod/group_vars/wireguard.yml```

Change the username ```secure_ssh_user``` (default 'user') and ```secure_ssh_identity_key``` in  ```./inventories/prod/group_vars/user.yml```

Launching playbooks:

```sh
1. sudo apt-get install sshpass
2. ansible-galaxy install --force --ignore-errors -r requirements.yml
3. ansible-playbook wireguard.yml -i inventories/prod/hosts
```
