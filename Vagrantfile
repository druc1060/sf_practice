# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"

   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y python3 python3-pip
     pip3 install Django
   SHELL
   config.vm.provision "file", source: "./file.txt", destination: "/home/vagrant/file.txt"
  end
end
