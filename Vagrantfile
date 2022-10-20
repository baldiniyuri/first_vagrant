# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
   
  # Windows 10 configuration.
    config.vm.define "windows10" do |win10|
      win10.vm.box = "Microsoft/EdgeOnWindows10"
      win10.vm.network "private_network", ip: "10.0.0.10" do |vb|
        vb.memory = "512"
        vb.cpus = 1
    end
  end

  # Ubuntu Server configuration
  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.network "private_network", ip: "10.0.0.20" do |vb|
      vb.memory = "512"
      vb.cpus = 1
  end
    ubuntu.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
    SHELL
end

  # CentOS configuration
  config.vm.define "centos" do |centos|
    centos.vm.box = "centos/7"
    centos.vm.network "private_network", ip: "10.0.0.30" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
  end
end

end