# [Ansible](https://www.ansible.com). Setup web-server. CentOS. + Wordpress + daily backup script

This Playbook deploy web-server running under CentOS:
- hostname
- create user
- Apache
- MySQL, mysql_secure_installation
- PHP
- SeLinux
- firewall
- install Wordpress
- cron (backup)

## Requirements
* SSH root access to the target servers. 

How to do that: Copy your public key to the target server with command below:
```
ssh-copy-id root_user@target.server.com
```

## Usage
* In ./ansible.cfg - check path to your private key and username 
* In ./group_vars/* - change the values of variables you need
* In ./hosts - define Hostname or IP of target servers
* Run Playbook:
```
ansible-playbook run.yml
```
