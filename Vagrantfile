# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM configuration.
  config.vm.box = "debian/buster64"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

  # node 1
  config.vm.define "node1" do |node|
    node.vm.hostname = "node1"
    node.vm.network :private_network, ip: "192.168.62.5"
  end 

  # node 2 
  config.vm.define "node2" do |node|
    node.vm.hostname = "node2"
    node.vm.network :private_network, ip: "192.168.62.6"
  end

  # node 3
  config.vm.define "node3" do |node|
    node.vm.hostname = "node3"
    node.vm.network :private_network, ip: "192.168.62.7"
  end
  # control
  config.vm.define "control" do |control|
    control.vm.hostname = "control"
    control.vm.network :private_network, ip: "192.168.62.8"
  end
end 

