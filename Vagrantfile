# -*- mode: ruby -*-
# vim: set ft=ruby :

Vagrant.configure("2") do |config|
	config.vm.box = "centos/7"
	config.vm.box_check_update = false
	config.vm.hostname = "nginx-fail2ban"
	config.vm.define "nginx"
	config.vm.provider "libvirt" do |vb|
	    vb.memory = 1024
	    vb.cpus = 2
	end
	config.vm.provision "shell", inline: <<-EOF
	    yum -y update
	    yum -y install mc bash-completion
	    mkdir -p ~root/.ssh
	    cp ~vagrant/.ssh/auth* ~root/.ssh/
	EOF
end
