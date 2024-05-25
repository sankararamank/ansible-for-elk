Vagrant.configure("2") do |config|
  config.ssh.forward_agent = true
  
  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "elasticsearch"
  config.vm.network "forwarded_port", guest: 22, host: 2215
  config.vm.network "forwarded_port", guest: 9200, host: 9200
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.synced_folder "~/.aws", "/home/vagrant/.aws"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
end
