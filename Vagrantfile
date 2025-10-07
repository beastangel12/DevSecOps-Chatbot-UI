Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  # Private network for Jenkins/Docker
  config.vm.network "private_network", ip: "192.168.56.10"

  # Allocate resources
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 2
  end

  # Provision using shell script (we’ll create it next)
  config.vm.provision "shell", path: "setup.sh"
end
