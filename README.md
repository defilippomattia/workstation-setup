# Introduction

Ansible and some other scripts for setting up a new linux workstation (Fedora).

# Ansible playbooks

```
sudo dnf install pipx                                                                   
pipx install --include-deps ansible

git clone https://github.com/defilippomattia/workstation-setup
cd workstation-setup

ansible-playbook ./ansible/000-packages/000-add-repos.yml -v --ask-become-pass
ansible-playbook ./ansible/000-packages/001-install-packages.yml -v --ask-become-pass
ansible-playbook ./ansible/000-packages/002-install-nvm.yml -v
ansible-playbook ./ansible/001-wifi-fix/000-wifi-fix.yml -v --ask-become-pass
ansible-playbook ./ansible/002-gui/000-gui.yml -v
```