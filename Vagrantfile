# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.
  config.vm.provision "shell", inline: "echo Hello"
  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.


  
  config.vm.define "ansible" do |ansible|
	ansible.vm.box = "bento/ubuntu-20.04"
	ansible.vm.network "public_network", ip: "192.168.0.25"
	ansible.vm.provider "virtualbox" do |vb|
		vb.name = 'ansible'
	end
	ansible.vm.provision "shell", inline: <<-SHELL
		sudo apt-get install -y net-tools
		sudo apt-get install -y default-jdk
		sudo apt-get install -y openssh-server
		apt-get install -y apache2
		apt-get -y install python-pip3
		pip3 install ansible
	   SHELL
	   
  end

  config.vm.define "foundtyvtt" do |foundtyvtt|
	foundtyvtt.vm.box = "bento/ubuntu-20.04"
	foundtyvtt.vm.network "public_network", ip: "192.168.0.30"
	foundtyvtt.vm.provider "virtualbox" do |vb|
		vb.name = 'foundtyvtt'
	end
	foundtyvtt.vm.provision "shell", inline: <<-SHELL
		sudo apt-get install -y net-tools
		sudo apt-get install -y default-jdk
		sudo apt-get install -y openssh-server
		apt-get install openssh-client
		ssh-keygen -t rsa
		
	   SHELL
	   
  end
end