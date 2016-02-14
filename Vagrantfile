# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box_check_update = false

  config.vm.define :dev_01 do |node|
    node.vm.box = "bento/centos-6.7"

    node.vm.network :forwarded_port, guest: 3000, host: 80
    node.vm.network :private_network, ip: "192.168.33.10"

    node.vm.provider :virtualbox do |vb|
      vb.memory = "2048"
    end

    node.push.define :atlas do |push|
      push.app = "ymkjp/bb"
    end

    node.vm.provision :ansible do |ansible|
      ansible.playbook = "provision/develop.yml"
    end
  end
end
