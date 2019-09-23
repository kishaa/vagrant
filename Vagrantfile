Vagrant.configure("2") do |config|
	config.vm.define :ubuntu do |ubuntu|
		ubuntu.vm.hostname = "ubuntu.ansible.client"
		ubuntu.vm.box = "kishaa/ansibleUbuntu14.04"
		ubuntu.vm.boot_timeout = 300
    ubuntu.vm.box_version = "1.0.1"
    ubuntu.vm.box_download_insecure = true
		# ubuntu.ssh.private_key_path = "C:\Users\KISHAN AGARWAL\Documents\centos.ppk"

		ubuntu.vm.network :private_network, ip: "192.168.111.21"
		ubuntu.vm.network :forwarded_port, guest: 2000, host: 8080,auto_correct: true
		ubuntu.vm.provider "virtualbox" do |prov|
			prov.customize ["modifyvm", :id, "--memory", "1024"]
#			prov.gui=true
			prov.name="ubuntu"
		end
	end
end


Vagrant.configure("2") do |config|
	config.vm.define :centos do |centos|
		centos.vm.hostname = "centos.ansible.client"
		centos.vm.box = "kishaa/ansibleCentos7"
		centos.vm.boot_timeout = 300
    centos.vm.box_version = "1.0.2"
    centos.vm.box_download_insecure = true
		centos.ssh.insert_key = false
		# centos.ssh.private_key_path = "C:\Users\KISHAN AGARWAL\Documents\centos.ppk"

		centos.vm.network :private_network, ip: "192.168.111.20"
		centos.vm.network :forwarded_port, guest: 2000, host: 8080,auto_correct: true
		centos.vm.provider "virtualbox" do |prov|
			prov.customize ["modifyvm", :id, "--memory", "1024"]
#			prov.gui=true
			prov.name="centos"
		end
	end
end

Vagrant.configure("2") do |config|
	config.vm.define :rhel7 do |rhel7|
		rhel7.vm.hostname = "rhel.ansible.manager"
		rhel7.vm.box = "kishaa/ansibleRHEL7"
		rhel7.vm.boot_timeout = 300
    rhel7.vm.box_version = "1.0.1"
    rhel7.vm.box_download_insecure = true
		rhel7.ssh.insert_key = false
		# rhel7.ssh.private_key_path = "C:\Users\KISHAN AGARWAL\Documents\rhel7.ppk"

		rhel7.vm.network :private_network, ip: "192.168.111.22"
		rhel7.vm.network :forwarded_port, guest: 2000, host: 8080,auto_correct: true
		rhel7.vm.provider "virtualbox" do |prov|
			prov.customize ["modifyvm", :id, "--memory", "1024"]
#			prov.gui=true
			prov.name="rhel7"
		end
	end
end
