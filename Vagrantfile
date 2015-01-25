# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "ubuntu/trusty64"

  # If true, agent forwarding over SSH connections is enabled. Defaults to false.
  config.ssh.forward_agent = true

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "shell", inline: <<PROVISIONSCRIPT
    curl -sL https://deb.nodesource.com/setup | sudo bash -
    sudo apt-get install -y nodejs build-essential
PROVISIONSCRIPT

  config.vm.hostname = '00-express-node-npm'
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
end
