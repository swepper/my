# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provision "file", source: "files/vagrant.pub", destination: "/home/vagrant/.ssh/"

  config.vm.define "server_myapp" do |server_myapp|
    server_myapp.vm.box = "bento/rockylinux-8"
    server_myapp.vm.hostname = "server-myapp"
#    server_postgres.vbguest.auto_update = false
    server_myapp.vm.network "private_network", ip: "192.168.56.67"
    server_myapp.vm.provision "shell", inline: <<-SHELL
    chmod 644 /home/vagrant/.ssh/vagrant.pub
    cat /home/vagrant/.ssh/vagrant.pub >> /home/vagrant/.ssh/authorized_keys
    SHELL
  end

end
