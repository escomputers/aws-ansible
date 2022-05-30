# Requirements
```
Python>=3.8
ansible=>5.8.0
ansible-core=>2.12.5
```
# 2) Create and configure ansible vault for storing credentials
```
#create vault, when asked enter a vault password
ansible-vault create group_vars/all/pass.yml

#add your root AWS account keys
ansible-vault edit group_vars/all/pass.yml

ec2_key: (your AWS account access key)
ec2_secret: (your AWS account secret key)
```
# 3) Set your desired settings into variables file
```
#edit file group_vars/all/vars.yml
```
# 4) Run playbook
```
ansible-playbook aws_setup.yml --ask-vault-pass
```
