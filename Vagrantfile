# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/debian-7.4"

  config.vm.network "private_network", ip: "192.168.33.55"

  # Install chef client (if necessary)
  config.vm.provision "shell", path: "scripts/install-chef.sh"

  config.vm.provision "chef_solo" do |chef|
    chef.custom_config_path = "Vagrantfile.chef"
    chef.cookbooks_path = "cookbooks"
    chef.add_recipe "apt"
    chef.add_recipe "grimoire::cvsanaly"
    chef.add_recipe "grimoire::mlstats"
  end
end
