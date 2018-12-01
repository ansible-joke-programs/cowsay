# Install Cowsay with Ansible

## Introduction

This program installs [Cowsay](https://github.com/tnalpgge/rank-amateur-cowsay) on CentOS7 or Ubuntu18.

## How To install

1. Install ansible and git

```
# CentOS7
sudo yum -y install epel-release git
sudo yum -y install ansible

# Ubuntu18
sudo apt update -y
sudo apt install -y language-pack-ja-base language-pack-ja
sudo apt install -y software-properties-common
sudo apt-add-repository -y ppa:ansible/ansible
sudo apt update -y
sudo apt install -y ansible
sudo apt install -y git
```

2. Execute playbook as root

```
git clone https://github.com/TomonoriMatsumura/ansible_joke-programs_cowsay.git
cd ansible_joke-programs_cowsay
ansible-playbook -i localhost install.yml
```

## CircleCI Test Coverage

Test is excuted on CircleCI with Docker container Centos7 latest Ansible installed: [tomonorimatsumura/centos7-ansible](https://hub.docker.com/r/tomonorimatsumura/centos7-ansible/)

[![CircleCI](https://circleci.com/gh/TomonoriMatsumura/ansible_joke-programs_cowsay.svg?style=svg)](https://circleci.com/gh/TomonoriMatsumura/ansible_joke-programs_cowsay)
