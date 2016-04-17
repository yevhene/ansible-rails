# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/precise64'

  config.vm.network 'forwarded_port', guest: 80, host: 8080

  config.vm.provision :server, type: :ansible do |ansible|
    ansible.playbook = 'provision/server.yml'
  end

  config.vm.provision :example_app, type: :ansible do |ansible|
    ansible.playbook = 'provision/app.yml'
    ansible.extra_vars = { app: 'example' }
  end
end
