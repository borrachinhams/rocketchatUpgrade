How to run
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

```
ansible-playbook -i hosts --ask-vault-pass -e "version=3.18.1" playbook.yml
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
