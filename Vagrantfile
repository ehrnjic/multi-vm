Vagrant.configure("2") do |c|
  c.vm.box = "debian/buster64"
  c.vm.provision "file", source: "./file_multi", destination: "~/file_multi"
  v.vm.box_check_update = false

  c.vm.define "vm1" do |vm1|
    vm1.vm.network "private_network", ip: "192.168.100.10"
    vm1.vm.network "forwarded_port", guest: 3000, host: 3000
    vm1.vm.provision "file", source: "./file_vm1", destination: "~/file_vm1" 
  end

  c.vm.define "vm2" do |vm2|
    vm2.vm.network "private_network", ip: "192.168.100.11"
    vm2.vm.network "forwarded_port", guest: 3000, host: 3001
    vm2.vm.provision "file", source: "./file_vm2", destination: "~/file_vm2"
  end
  
end
