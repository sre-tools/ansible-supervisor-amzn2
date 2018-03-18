# Ansible role for Supervisor


This role will install [Supervisor](https://supervisord.org/), a process 
control system


#### Tested on

  * Amazon Linux 2 EC2 Instance


#### Defaults

  * `supervisor_services`: `{welcome.conf}`


#### Usage

Services are configured using the `supervisor_services` hash,
in which every entry is a different service. In turn, you can
specify any supervisor parameter you need.


#### Running a command
Refer this [playbook](https://github.com/sre-tools/ansible-supervisor-amzn2/blob/master/playbook.yml)

```
`---
- hosts: localhost
  become: yes
  roles:
   - role: ansible-supervisor-amzn2
```

#### Sample monitored program
Refer this [welcome.conf](https://github.com/sre-tools/ansible-supervisor-amzn2/blob/master/ansible-supervisor-amzn2/templates/etc/supervisor/conf_d/welcome.conf.j2)

Note: extension should be is .conf<br />
logs for this sample app are stored in /var/log/welcome

#### Include directory for monitoring
```
/etc/supervisor/conf_d/
```

####Requirements
```bash
Python 2.7
pip
ansible 2.4
```
**Read more on [Supervisor on AWS Linux AMI](https://ls3.io/post/supervisor_on_aws_linux_ami/)**<br />
[Above link in local]()