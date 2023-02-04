# Version: 0.1.0
Vagrant.configure("2") do |config|
  config.vm.synced_folder '.', '/vagrant', disabled: true
  
  config.vm.box = "prof-ninjason/pfsense"
  config.vm.hostname = "pfsense"

  #config.vm.network "forwarded_port", guest: 22, host: 2222
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 443, host: 8443
  
  config.ssh.username = 'vagrant'
  config.ssh.password = 'vagrant'
  
  config.vm.network "private_network", type: "dhcp", virtualbox__intnet: true

  config.vm.provider "virtualbox" do |vb|
    vb.name = "pfSense"
	vb.memory = "2048"
  	vb.cpus = "2"
  end
end
