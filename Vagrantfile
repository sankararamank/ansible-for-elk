Vagrant.configure("2") do |config|
  config.ssh.forward_agent = true
  
  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "elk-node"
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.network "forwarded_port", id: "elasticsearch1", guest: 9200, host: 9200
  config.vm.network "forwarded_port", id: "elasticsearch2", guest: 9300, host: 9300
  config.vm.synced_folder "~/.aws", "/home/vagrant/.aws"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
end
