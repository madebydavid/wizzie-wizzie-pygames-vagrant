# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

    config.vm.box = "precise64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"

    config.vm.network "forwarded_port", guest: 80, host: 8888

    config.vm.provision :shell, :path => "bootstrap.sh"

    config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777"]

    config.ssh.forward_agent = true

    config.vm.provider :virtualbox do |vb|
        vb.gui = true
    end

end
