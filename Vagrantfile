Vagrant.configure("2") do |config|
  config.vm.define "mysql-vm" do |vm1|
    vm1.vm.box = "debian/jessie64"
    vm1.vm.hostname= "mysql-vm"
    vm1.vm.network "private_network", ip: "192.168.56.10" 
    vm1.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("#{Dir.home}/.ssh/id_rsa.pub").first.strip
      s.inline = <<-SHELL
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
        sudo apt-get install -y python3
      SHELL
    end
    vm1.vm.provider "virtualbox" do |vb|
      vb.name = "mysql-vm"
      vb.memory = 1024
      vb.cpus = 1
    end
  end
 
  config.vm.define "laravel-vm" do |vm1|
    vm1.vm.box = "debian/jessie64"
    vm1.vm.hostname= "laravel-vm"
    vm1.vm.network "private_network", ip: "192.168.56.20" 
    vm1.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("#{Dir.home}/.ssh/id_rsa.pub").first.strip
      s.inline = <<-SHELL
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
        sudo apt-get install -y python3
      SHELL
    end
    vm1.vm.provider "virtualbox" do |vb|
        vb.name = "laravel-vm"
        vb.memory = 1024
        vb.cpus = 1
    end
  end

  config.vm.define "angular-vm" do |vm1|
    vm1.vm.box = "debian/jessie64"
    vm1.vm.hostname= "angular-vm"
    vm1.vm.network "private_network", ip: "192.168.56.30" 
    vm1.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("#{Dir.home}/.ssh/id_rsa.pub").first.strip
      s.inline = <<-SHELL
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
        sudo apt-get install -y python3
      SHELL
    end
    vm1.vm.provider "virtualbox" do |vb|
        vb.name = "angular-vm"
        vb.memory = 1024
        vb.cpus = 1
    end
  end

  config.vm.define "gitlab-vm" do |vm1|
    vm1.vm.box = "debian/jessie64"
    vm1.vm.hostname= "gitlab-vm"
    vm1.vm.network "private_network", ip: "192.168.56.30" 
    vm1.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("#{Dir.home}/.ssh/id_rsa.pub").first.strip
      s.inline = <<-SHELL
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
        sudo apt-get install -y python3
      SHELL
    end
    vm1.vm.provider "virtualbox" do |vb|
        vb.name = "gitlab-vm"
        vb.memory = 1024
        vb.cpus = 1
    end
  end
end