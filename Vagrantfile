# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.30.2"
  config.vm.provider :libvirt do |v|
    v.memory = 1024
  end
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "dhcpd/tests/test.yml"
  end
end
