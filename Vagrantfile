Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |v|
    v.memory = 256
    v.cpus = 1
  end

  config.vm.define :balancer do |ng|
    ng.vm.hostname = "balancer"
    ng.vm.network "private_network", ip: "192.168.10.10"
  end

  config.vm.define :app do |app|
    app.vm.hostname = "app-backend"
    app.vm.network "private_network", ip: "192.168.10.11"
  end

end
