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
git clone https://github.com/TomonoriMatsumura/ansible_joke-programs_cowsay.git
cd ansible_joke-programs_cowsay
ansible-playbook -i localhost install.yml
```

## CircleCI Test Coverage

Test is excuted on Docker container Centos7 latest Ansible installed wtih CircleCI: [tomonorimatsumura/centos7-ansible](https://hub.docker.com/r/tomonorimatsumura/centos7-ansible/)

[![CircleCI](https://circleci.com/gh/TomonoriMatsumura/ansible_joke-programs_cowsay/tree/topic.svg?style=svg)](https://circleci.com/gh/TomonoriMatsumura/ansible_joke-programs_cowsay/tree/topic)
