## Ansible PlayBook To Install Wordpress In Amazon Linux Ec2

This ansible playbook will install full Lampstack and latest wordpress on aws ec2 running amzn2.


#### - Download the git repo.

This ansible playbook is a fork from the following repository:

```
[gnu]$ git clone git@github.com:beingarju/ansible-amazon-linux-wordpress.git
```

```
[gnu]$ cd ansible-amazon-linux-wordpress
```

### - Edit the hosts file as your need.

- EIP = External IP of your Ec2.
- KeyPath = private key path.

```
[webserver]
EIP  ansible_port=22  ansible_user='ec2-user'  ansible_ssh_private_key_file='KeyPath'

```
### - Run The PlayBook

```
ansible-playbook -i hosts wordpress.yml
```
