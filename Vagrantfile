# -*- mode: ruby -* 
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.ssh.insert_key = false
    config.vm.synced_folder ".", "/vagrant", disabled: true
    config.vm.provider :virtualbox do |v|
        v.memory = 1024
        v.linked_clone = true
        v.gui = true
        v.cpus = 2
    end

    # App Server 1
    config.vm.define "srv1" do |ubuntu1804|
        ubuntu1804.vm.box = "generic/ubuntu1804"
        ubuntu1804.vm.hostname = "ubuntu1804.test"
        ubuntu1804.vm.network :private_network, ip: "192.168.56.4"
    end

    # App Server 2
    config.vm.define "srv2" do |ubuntu2010|
        ubuntu2010.vm.box = "generic/ubuntu2010"
        ubuntu2010.vm.hostname = "ubuntu2010.test"
        ubuntu2010.vm.network :private_network, ip: "192.168.56.5"
    end

    # App Server 3
    config.vm.define "srv3" do |ubuntu2204|
        ubuntu2204.vm.box = "generic/ubuntu2204"
        ubuntu2204.vm.hostname = "ubuntu2204.test"
        ubuntu2204.vm.network :private_network, ip: "192.168.56.6"
    end

    # App Server 4
    config.vm.define "srv4" do |centos|
        centos.vm.box = "generic/centos7"
        centos.vm.hostname = "centos.test"
        centos.vm.network :private_network, ip: "192.168.56.7"
    end
end