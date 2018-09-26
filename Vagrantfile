Vagrant.require_version ">= 2.1.5"
Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vagrant.plugins = ["vagrant-reload", "vagrant-vbguest"]
    config.ssh.forward_agent = true
    config.vbguest.auto_update = true
    config.vm.network "private_network", ip: "192.168.50.51"
    config.vm.provider "virtualbox" do |v|
        v.name = "W3C_Validator_Ubuntu_18.04"
        v.gui = false
        v.memory = 2048
        v.cpus = 2
    end
    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    config.vm.provision :shell, path: "bootstrap.sh"
    config.vm.provision :reload
end
