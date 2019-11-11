Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.define "master" do |master|
  config.disksize.size = '50GB'

    master.vm.box = "ubuntu/bionic64"
    master.vm.hostname = "master"
    master.vm.network :public_network, type: "dhcp"
    master.vm.network :private_network, ip: "192.168.12.50", virtualbox__vboxnet0: true
  end

config.vm.define "client" do |client|
    client.vm.box = "ubuntu/bionic64"
    client.vm.hostname = "client"
    client.vm.network :public_network, type: "dhcp"
    client.vm.network :private_network, ip: "192.168.12.51", virtualbox__vboxnet0: true
  end

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "3330"]
  end

end


