## How to install wireguard

The inventory is on the way ```./inventories/prod/hosts``` . Change the IP address, name of the VM and ```ansible_ssh_user``` (default 'user').

Change the variable ```docker_users``` (default 'user')  ```./inventories/prod/group_vars/wireguard.yml```

Change the username ```secure_ssh_user``` (default 'user') and ```secure_ssh_identity_key``` in  ```./secure-ssh.yml```

Install the ssh key for the root user ```ssh-copy-id -i /home/$USER/.ssh/id_rsa.pub root@5.55.55.555```

Launching playbooks:

```sh
1. ansible-galaxy install --force --ignore-errors -r requirements.yml
2. ansible-playbook secure-ssh.yml -i inventories/prod/hosts
3. ansible-playbook wireguard.yml -i inventories/prod/hosts
```
