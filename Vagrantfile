# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.synced_folder '.', '/vagrant', disabled: false

  config.vm.define "skeleton" do |app|
    app.vm.hostname = "skeleton"
    app.vm.box = "precise64"
    app.vm.box_url = "http://files.vagrantup.com/precise64.box"

    app.vm.network :private_network, ip: "10.11.12.25"
    app.vm.network :forwarded_port, guest: 80, host: 3001

    app.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--memory", 512]
    end
  end
  
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "vagrant.yml"
    ansible.inventory_path = "vagrant"
  end

end
