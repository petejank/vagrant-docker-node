# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.boot_timeout = 10000

  # Box to build off of.
  config.vm.box = "ubuntu/disco64"

  config.disksize.size = '30GB'

  # The hostname of the machine.
  config.vm.hostname = "vagrantdockernode.dev"

  # config.vm.network "forwarded_port", guest: 8080, host: 8080

  # Configures networks on the machine.
  config.vm.network :private_network, ip: "10.0.0.100"

  # Configures synced folders.
  config.vm.synced_folder "sync", "/sync"

  # Configures provisioners.
  config.vm.provision :shell, :path => "bootstrap.sh"

end
