How to
=========

After download the program, create file with name hosts and put the information for connect the hosts. Ex:

```bash
[rocketchat]
10.10.10.10

[rocketchat:vars]
ansible_ssh_port=22
ansible_ssh_user=user
ansible_ssh_pass='mypass'
ansible_become=yes
ansible_become_method=su
ansible_become_exe='su -'
ansible_become_pass='myRootPass'
```

Now you need run the command:
In this example I will use the ansible vault, if not, just remove the `--ask-vault-pass line`

```
ansible-playbook -i hosts --ask-vault-pass -e "version=4.0.3" playbook.yml
```

License
-------

BSD