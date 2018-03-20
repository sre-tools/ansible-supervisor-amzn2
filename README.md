# Ansible role for Supervisor


This role will install [Supervisor](https://supervisord.org/), a process 
control system


#### Tested on

  * Amazon Linux 2 [EC2 Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/amazon-linux-2-virtual-machine.html)


#### Usage

Apps are configured as [subprocesses](http://supervisord.org/subprocess.html#subprocesses) using the '.conf' file as per supervisor config [format](http://supervisord.org/configuration.html#file-format),
refer [Include](https://github.comcast.com/xh-pod/ansible-supervisor-amzn2/tree/master/ansible-supervisor-amzn2#include-directory-for-monitoring) section below


#### Running a command
<small>Refer this [playbook](https://github.comcast.com/xh-pod/ansible-supervisor-amzn2/blob/master/playbook.yml)</small>

```
`---
- hosts: localhost
  become: yes
  roles:
   - role: ansible-supervisor-amzn2
```

#### Sample monitored program
Refer this [welcome.conf](https://github.comcast.com/xh-pod/ansible-supervisor-amzn2/blob/master/ansible-supervisor-amzn2/templates/etc/supervisor/conf_d/welcome.conf.j2)<br/>
<small>**Notes**:</small><br />
<sub>extension should be is .conf</sub><br />
<sup>logs for this sample app are stored in /var/log/welcome</sup><br />
<small>must create 'welcome' folder before enabling logs</small>

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
<sup>[Above link in local](https://github.comcast.com/xh-pod/ansible-supervisor-amzn2/tree/master/ansible-supervisor-amzn2/meta)</sup>