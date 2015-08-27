# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "trusty64"
    config.vbguest.auto_update = true
    config.vbguest.auto_reboot = true
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbooks/update_galaxy.yml"
    end
end
