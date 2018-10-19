# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 8001, host: 8001
  config.vm.provision "docker"
  config.vm.provision "shell" do |s|
    s.path = "provision.sh"
  end
  
end
