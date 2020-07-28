# Ansible script for setting up Linux desktop environment

## Prerequisites

The following things need to be setup on local machine (the one being setup).

### Ansible

```commandline
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
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