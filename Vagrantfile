
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  # Hack the ethernet address to be the same
  config.vm.network "public_network", :mac => "5254004d77d3"
  
  config.vm.network "forwarded_port", guest: 8080, host: 9001
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "4096"
  end

  config.vm.provision "shell", inline: <<-SHELL
    echo "Starting install"
    yum upgrade -y
    yum install -y net-tools libSM libXrender xterm emacs
    yum install -y /vagrant/diamond_3_12-base-240-2-x86_64-linux.rpm
    cp /vagrant/lisense.dat /usr/local/diamond/3.12/license/
  SHELL
end
