# Ansible role for reversing Supervisor


This role will uninstall [Supervisor](https://supervisord.org/), a process 
control system


#### Tested on

  * Amazon Linux 2 EC2 Instance


#### Running a command
<small>Refer this [playbook](https://github.com/sre-tools/ansible-supervisor-amzn2/blob/master/playbook.yml)</small><br/>
```
`---
- hosts: localhost
  become: yes
  roles:
   - role: cleanup
```

####Requirements
```bash
Python 2.7
pip
ansible 2.4
```