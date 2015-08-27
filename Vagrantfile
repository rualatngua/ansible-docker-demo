# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    # Ubuntu 14.04 is capable of running docker without any kernel modifications
    config.vm.box = "ubuntu/trusty64"
    
    config.vbguest.auto_update = true
    config.vbguest.auto_reboot = true
    
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbooks/update_galaxy.yml"
    end
end
