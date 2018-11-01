# -*- mode: ruby -*-
# vi: set ft=ruby :

#require necessary plugins
required_plugins = %w( vagrant-hostmanager vagrant-vbguest )
required_plugins.each do |plugin|
  system "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end

Vagrant.configure("2") do |config|

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.include_offline = true

  config.vm.define "mon1" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.11", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.11", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "mon1.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
  config.vm.define "mon2" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.12", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.12", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "mon2.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
  config.vm.define "mon3" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.13", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.13", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "mon3.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
  config.vm.define "osd1" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.21", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.21", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "osd1.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
  config.vm.define "osd2" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.22", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.22", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "osd2.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
  config.vm.define "osd3" do |b|
    b.vm.box = "ubuntu/xenial64" # 16.04
    b.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = "1"
    end
    b.vm.synced_folder ".", "/vagrant", disabled: true
    b.vm.synced_folder "ansible", "/vagrant/ansible", create: true, owner: "vagrant", group: "vagrant", mount_options: ["dmode=775,fmode=775"]
    b.vbguest.auto_update = true

    b.vm.network "private_network", ip: "192.168.16.23", netmask: "255.255.255.0"
    b.vm.network "private_network", ip: "192.168.32.23", netmask: "255.255.255.0", virtualbox__intnet: "ceph"

    b.vm.hostname = "osd3.lokal"

    b.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.install_mode = :pip
      ansible.version = "latest"
      ansible.playbook = "ansible/all.yml"
      ansible.galaxy_role_file = "ansible/requirements.yml"
    end
  end
end
