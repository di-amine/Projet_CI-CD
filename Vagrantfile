Vagrant.configure("2") do |config|

    # Linux OS CentOS
    config.vm.box = "geerlingguy/centos7"

    config.vm.network "public_network"
  
    # jenkins server
    config.vm.define "jenkins-server" do |jenkins|
      jenkins.vm.hostname = "jenkins.dev"
      # static ip address
      jenkins.vm.network :private_network, ip: "192.168.60.2"
      jenkins.vm.network :forwarded_port, guest: 80, host: 8002
    end
      
    # docker server
    config.vm.define "docker-server" do |docker|
      docker.vm.hostname = "docker.dev"
      # static ip address
      docker.vm.network :private_network, ip: "192.168.60.3"
      docker.vm.network :forwarded_port, guest: 80, host: 8003
    end

    # kubernetes server
    config.vm.define "kube-server" do |kube|
        kube.vm.hostname = "kube.dev"
        # static ip address
        kube.vm.network :private_network, ip: "192.168.60.4"
        kube.vm.network :forwarded_port, guest: 80, host: 8004
    end
end