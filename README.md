# README

## Setup

### Ansible
```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

### Create inventory
**inventories/your-inventory**
```
[example]
example.com

[example:vars]
app=example
```

### Run playbook
```
ansible-playbook -i inventories/your-inventory provision/your-playbook.yml
```

## Vagrant

### Setup

#### Dependencies
```
sudo apt-get install vagrant virtualbox
```

#### Run
```
vagrant up
```

### Tasks

#### Provision
```
vagrant provision
```
