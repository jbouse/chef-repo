# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "precise64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.hostname = "#{%x{whoami}.chomp}-vagrant.atl.undergrid"

  # Enable provisioning with chef solo, specifying a cookbooks path, roles
  # path, and data_bags path (all relative to this Vagrantfile), and adding
  # some recipes and/or roles.
  #
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = [:vm, "/vagrant"]
    chef.roles_path = [:vm, "/vagrant"]
    chef.data_bags_path = [:vm, "/vagrant"]
  #   chef.add_recipe "mysql"
  #   chef.add_role "web"

    # You may also specify custom JSON attributes:
  #   chef.json = { :mysql_password => "foo" }
  end
end
