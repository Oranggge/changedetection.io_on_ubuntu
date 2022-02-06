# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
  end
  
  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "geerlingguy/ubuntu2004"
    ubuntu.vm.hostname = "ubuntu.os"
    ubuntu.vm.network "private_network", ip: "192.168.60.6"
  end
end
