# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048" # 2 GB RAM
    vb.cpus = 2
  end

  config.vm.network "private_network", type: "dhcp"

  config.vm.provision "shell", inline: <<-SHELL
    sudo yum update -y
    
    sudo yum install -y python3
    
    sudo yum install -y vim
    
    echo "export EDITOR=vim" >> /home/vagrant/.bashrc
    source /home/vagrant/.bashrc
  SHELL
end
