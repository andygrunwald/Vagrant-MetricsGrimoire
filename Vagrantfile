# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/debian-7.4"

  config.vm.network "private_network", ip: "192.168.33.55"

  # Install chef client
  config.vm.provision "shell" do |s|
    s.inline = "curl -L https://www.opscode.com/chef/install.sh | sudo bash"
  end

  config.vm.provision "chef_solo" do |chef|
    chef.cookbooks_path = "cookbooks"
    chef.add_recipe "cvsanaly"
    chef.json = {
      :repositoryhandler => {
        :destination => '/tmp/MetricsGrimoire/RepositoryHandler',
        :owner => 'vagrant',
        :group => 'vagrant'
      },
      :cvsanaly => {
        :destination => '/tmp/MetricsGrimoire/CVSAnalY',
        :owner => 'vagrant',
        :group => 'vagrant'
      },
    }
  end
end
