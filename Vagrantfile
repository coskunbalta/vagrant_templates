Vagrant.configure("2") do |config|
  config.vm.define "web1" do |web1|
    web1.vm.box = "npalm/mint17-amd64-cinnamon"
    web1.vm.hostname = 'web'
    web1.vm.box_url = "npalm/mint17-amd64-cinnamon"

    web1.vm.network :private_network, ip: "192.168.56.101"

    web1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "web1"]
      v.customize ["modifyvm", :id, "--cpus", 2]
    end
  end
end
