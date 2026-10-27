# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"
  config.vm.boot_timeout = 600

  # jumpbox
  config.vm.define "jumpbox" do |jumpbox|
    jumpbox.vm.hostname = "jumpbox"
    jumpbox.vm.network "private_network", ip: "192.168.10.100"

    jumpbox.vm.provider "virtualbox" do |vb|
      vb.name = "jumpbox"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  # server
  config.vm.define "server" do |server|
    server.vm.hostname = "server"
    server.vm.network "private_network", ip: "192.168.10.101"


    server.vm.provider "virtualbox" do |vb|
      vb.name = "server"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # node 0
  config.vm.define "node-0" do |node_0|
    node_0.vm.hostname = "node-0"
    node_0.vm.network "private_network", ip: "192.168.10.102"

    node_0.vm.provider "virtualbox" do |vb|
      vb.name = "node-0"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # node 1
  config.vm.define "node-1" do |node_1|
    node_1.vm.hostname = "node-1"
    node_1.vm.network "private_network", ip: "192.168.10.103"

    node_1.vm.provider "virtualbox" do |vb|
      vb.name = "node-1"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

end
