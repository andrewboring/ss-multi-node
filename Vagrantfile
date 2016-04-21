# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|


  config.vm.define "ssnode1" do |node1|
    node1.vm.box = "centos/7"
    node1.vm.hostname = "ssnode1" 
    node1.vm.network "private_network", type: "dhcp"


    node1.vm.provider "virtualbox" do |vb|
      vb.gui = true
      vb.memory = "1024"

      vb.customize ['storagectl', :id, '--name', 'SATA', '--add', 'sata', '--controller', 'IntelAHCI', '--portcount', 3]
      vb.customize ['createmedium', 'disk', '--filename', './n1disk1.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 0, '--device', 0, '--type', 'hdd', '--medium', './n1disk1.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n1disk2.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', './n1disk2.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n1disk3.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', './n1disk3.vdi']
    end
    node1.vm.provision "shell", inline: <<-SHELL
      yum -y update
      yum -y install net-tools
      curl https://platform.swiftstack.com/install | bash
      echo "ssclaimurl" >> /home/vagrant/.bashrc
    SHELL
  end

  config.vm.define "ssnode2" do |node2|
    node2.vm.box = "centos/7"
    node2.vm.hostname = "ssnode2"
    node2.vm.network "private_network", type: "dhcp"


    node2.vm.provider "virtualbox" do |vb|
      vb.gui = true
      vb.memory = "1024"

      vb.customize ['storagectl', :id, '--name', 'SATA', '--add', 'sata', '--controller', 'IntelAHCI', '--portcount', 3]
      vb.customize ['createmedium', 'disk', '--filename', './n2disk1.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 0, '--device', 0, '--type', 'hdd', '--medium', './n2disk1.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n2disk2.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', './n2disk2.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n2disk3.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', './n2disk3.vdi']
    end
    node2.vm.provision "shell", inline: <<-SHELL
      yum -y update
      yum -y install net-tools
      curl https://platform.swiftstack.com/install | bash
      echo "ssclaimurl" >> /home/vagrant/.bashrc
    SHELL
  end

  config.vm.define "ssnode3" do |node3|
    node3.vm.box = "centos/7"
    node3.vm.hostname = "ssnode3"
    node3.vm.network "private_network", type: "dhcp"


    node3.vm.provider "virtualbox" do |vb|
      vb.gui = true
      vb.memory = "1024"

      vb.customize ['storagectl', :id, '--name', 'SATA', '--add', 'sata', '--controller', 'IntelAHCI', '--portcount', 3]
      vb.customize ['createmedium', 'disk', '--filename', './n3disk1.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 0, '--device', 0, '--type', 'hdd', '--medium', './n3disk1.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n3disk2.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', './n3disk2.vdi']
      vb.customize ['createmedium', 'disk', '--filename', './n3disk3.vdi', '--size', 1024]
      vb.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', './n3disk3.vdi']
    end
    node3.vm.provision "shell", inline: <<-SHELL
      yum -y update
      yum -y install net-tools
      curl https://platform.swiftstack.com/install | bash
      echo "ssclaimurl" >> /home/vagrant/.bashrc
    SHELL
  end


  #config.vm.provision "shell", inline: <<-SHELL
  #    yum -y update 
  #    yum -y install net-tools
  #    curl https://platform.swiftstack.com/install | bash
  #     echo "ssclaimurl" >> /home/vagrant/.bashrc
  #SHELL


end
