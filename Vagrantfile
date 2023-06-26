Vagrant.configure("2") do |config|
  # Distro Linux
  config.vm.box = "ubuntu/focal64"
  # Network
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.network "public_network"
  # Folder 
  config.vm.synced_folder "./Data", "/vagrant_data"
  # System
  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true
  
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
    vb.cpus = 2
    vb.name = "Ubuntu CTF"
  end


  config.vm.provision "shell", inline: <<-SHELL
    apt-get update && apt upgrade -y
    apt-get install -y apache2 mysql-client mysql-server
    timedatectl set-timezone Asia/Ho_Chi_Minh
  SHELL

  # config.vm.provision "shell", path: "./Ubuntu/install_docker"
end
