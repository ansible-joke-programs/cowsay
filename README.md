# Install Cowsay on CentOS7 with Ansible

## Introduction

This program installs [Cowsay](https://github.com/tnalpgge/rank-amateur-cowsay) on CentOS7.

## How To install

1. install ansible

```
sudo yum -y install epel-release
sudo yum -y install ansible
```

2. excute playbook as root

```
git clone https://github.com/TomonoriMatsumura/ansible_joke-program_cowsay.git
cd ansible_joke-program_cowsay
ansible-playbook -i localhost install.yml
```
