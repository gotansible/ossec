# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
	config.vm.define "ossec" do |ossec|
		ossec.vm.hostname = "ossec"
		ossec.vm.box = "hashicorp/precise64"
		ossec.vm.provision :ansible do |ansible|
			ansible.playbook = "test-server.yml"
		end
		ossec.vm.network "private_network", ip: "192.168.50.30"
	end

	config.vm.define "agent" do |agent|
		agent.vm.hostname = "agent"
		agent.vm.box = "chef/centos-6.5"
		#agent.vm.box = "hashicorp/precise64"
		agent.vm.provision :ansible do |ansible|
			ansible.playbook = "test-agent.yml"
		end
		agent.vm.network "private_network", ip: "192.168.50.31"
	end
end
