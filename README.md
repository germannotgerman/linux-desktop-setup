# Ansible script for setting up Linux desktop environment

This script will execute locally, meaning **on the same workstation where you are executing the script from**.

## Prerequisites

The following things need to be setup on local machine (the one being setup).

### Ansible

```commandline
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```

### Ansible user
You need to create Ansible user and give it sudo rights. In addition for things to run smoothly add NOPASS option.
```commandline
sudo useradd ansible
sudo usermod -aG sudo ansible
sudo visudo
```  
In the last step a file will be opened. There add the following line for ansible user if not already there:
```commandline
ansible ALL=(ALL)       NOPASSWD: ALL
```  

### Ansible roles

```commandline
ansible-galaxy install geerlingguy.java
ansible-galaxy install geerlingguy.docker
ansible-galaxy install ansible-role-install-snap
ansible-galaxy install ngetchell.vscode
ansible-galaxy install pixelart.chrome
ansible-galaxy install viasite-ansible.zsh
```

## Executing script

```commandline
cd linux-desktop-setup/ansible
ansible-playbook setup-desktop-environment.yml
```
