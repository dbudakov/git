# -*- mode: ruby -*-
# vi: set ft=ruby:
Vagrant.configure("2") do |config|
	config.vm.define "os" do |os|
		os.vm.box = "centos/7"
		os.vm.host_name = "git"
		os.vm.network  "private_network", ip: '192.168.100.205'
		os.vm.provider :virtualbox do |vb|
			vb.customize ["modifyvm", :id, "--memory", "256"]
		end
		os.vm.provision "shell", inline: <<SHELL
		sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
		sed -i 's/#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config
		systemctl restart sshd
SHELL
	end
## Устанавливаем связь между каталогом "./src" хост-системы
## и каталогом "/home/vagrant" гостевой системы.
#		config.vm.synced_folder "./src", "/home/vagrant"
end
