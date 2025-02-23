## About
This repository contains Ansible playbooks to automate server setup.

## Install Ansible on Ubuntu
Run the following commands to install Ansible on ubuntu:
```bash
$ sudo apt update
$ sudo apt install -y software-properties-common
$ sudo add-apt-repository --yes --update ppa:ansible/ansible
$ sudo apt install -y ansible
```
**command- Running the Ansible Playbook**
```
ansible-playbook -i inventory filename.yml
```
**define inventory—the list of managed hosts**
```
$ nano inventory.ini
```
**list hosts in it**
```
[localhost]
127.0.0.1
[webservers]
private_ip_of_host_server ansible_ssh_user=ubuntu ansible_private_key_file=privatekey_of_host
