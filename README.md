# README

## Setup

### Ansible
```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

## Provision

### Create inventory
**inventories/your-inventory**
```
[example]
example.com

[example:vars]
app=example
domain=example.com
ansible_user=root
ansible_connection=ssh
```

### Setup server
```
ansible-playbook -i inventories/your-inventory provision/server.yml
```

### Setup app
```
ansible-playbook -i inventories/your-inventory provision/app.yml
```

## Vagrant

### Setup
```
sudo apt-get install vagrant virtualbox
```

### Run
```
vagrant up
```

### Tasks

#### Provision
```
vagrant provision
```
