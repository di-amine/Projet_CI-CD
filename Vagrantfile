Vagrant.configure("2") do |config|

  # Linux OS CentOS
  config.vm.box = "geerlingguy/centos7"
  config.vm.network "public_network" 
  # nexus server
  config.vm.define "nexus-server" do |nexus|
    nexus.vm.hostname = "nexus.dev"
    # static ip address
    nexus.vm.network :private_network, ip: "192.168.60.5"
    nexus.vm.network :forwarded_port, guest: 80, host: 8005

  end
    
  
  # Database server
  config.vm.define "mangodb-server" do |mangodb|
    mangodb.vm.hostname = "mangodb.dev"
    # static ip address
    mangodb.vm.network :private_network, ip: "192.168.60.6"
    mangodb.vm.network :forwarded_port, guest: 80, host: 8006
    
  end

end
