[![](https://github.com/ansible-joke-programs/cowsay/workflows/build/badge.svg)](https://github.com/ansible-joke-programs/cowsay/actions?query=workflow%3Abuild)

# Ansible Playbook - cowsay

## Introduction

This program installs [cowsay](https://github.com/tnalpgge/rank-amateur-cowsay) on CentOS7/CentOS8.

![cowsay](https://user-images.githubusercontent.com/1615430/49337490-bdfe9a80-f656-11e8-8265-37d140302a31.gif)

Parameters (See for more details [cowsay - Wikipedia](https://en.wikipedia.org/wiki/Cowsay "cowsay - Wikipedia"))

| Option | Purpose |
| --- | --- |
| -n | Disables word wrap, allowing the cow to speak FIGlet or to display other embedded ASCII art. Width in columns becomes that of the longest line, ignoring any value of -W. |
| -W | Specifies width of the speech balloon in columns, i.e. characters in a monospace font. Default value is 40. |
| -b | “Borg mode”, uses == in place of oo for the cow′s eyes. |
| -d | “Dead”, uses XX, plus a descending U to represent an extruded tongue, also used on Linux kernel oops. |
| -g | “Greedy”, uses $$. |
| -p | “Paranoid”, uses @@. |
| -s |“Stoned”, uses ** to represent bloodshot eyes, plus a descending U to represent an extruded tongue. |
| -t | “Tired”, uses --. |
| -w | “Wired”, uses OO. |
| -y | “Youthful”, uses .. to represent smaller eyes. |
| -e eye_string | Manually specifies the cow′s eye-type, e.g. cowsay -e ^^ (see Eastern-style emoticon).[5] |
| -T tongue_string | Manually specifies the cow′s tongue shape, e.g. cowsay -T \(\) for a pair of parentheses.[5] |
| -f cowfile | Specifies a .cow file from which to load alternative ASCII art. Accepts both absolute file-paths and those relative to the environment variable COWPATH. |
| -l | Lists the names of available cow-files in the COWPATH directory instead of displaying a quote. |



## How To install

1. Install ansible and git

```
sudo yum -y install epel-release git
sudo yum -y install ansible
```

2. Execute playbook as root

```
git clone https://github.com/ansible-joke-programs/cowsay.git
cd cowsay
ansible-galaxy install -r roles/requirements.yml
ansible-playbook -i localhost, -c local install.yml
```
