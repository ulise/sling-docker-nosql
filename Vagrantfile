# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "private_network", ip: "192.168.100.20"
    config.vm.provision "docker" do |d|
   #   d.build_image "/vagrant/container"
    end
	config.vm.provider "virtualbox" do |v|
		v.gui = false
		v.memory = 2048
		v.cpus = 2
	end
end
