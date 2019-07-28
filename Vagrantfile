# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRATFILE_API_VERSION = "2"

Vagrant.configure(VAGRATFILE_API_VERSION) do |config|
  # General config
  config.vm.box = "geerlingguy/centos7"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 256
    v.linked_clone = true
  end

# Applicatio server 1
  config.vm.define "app1" do |app|
    app.vm.hostname = "orc-app1.test"
    app.vm.network :private_network , ip: "192.168.60.4"
  end

# Applicatio server 2
  config.vm.define "app2" do |app|
    app.vm.hostname = "orc-app2.test"
    app.vm.network :private_network , ip: "192.168.60.5"
  end


# Database server 1
  config.vm.define "db" do |db|
    db.vm.hostname = "orc-db.test"
    db.vm.network :private_network , ip: "192.168.60.6"
  end
end
