# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do|config|
	config.ssh.insert_key = false
	config.vm.provider :virtualbox do|vb|
		vb.customize ["modifyvm", :id, "--memory", "2048"]
	end
	
	#Application Server1
	config.vm.define "app1" do|app|
		app.vm.hostname = "mwiapp04"
		app.vm.box = "geerlingguy/centos7"
		app.vm.network "public_network", ip: "192.168.43.15"
	end
  

	#Application Server2
	config.vm.define "app2" do|app|
		app.vm.hostname = "mwiapp05"
		app.vm.box = "geerlingguy/centos7"
		app.vm.network "public_network", ip: "192.168.43.16"
	end

	config.vm.box_check_update = false
	config.vbguest.auto_update = false

end

