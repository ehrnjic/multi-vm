Vagrant.configure("2") do |c|
  c.vm.box = "debian/buster64"
  c.vm.define "vm1" do |vm1|
    c.vm.network "forwarded_port", guest: 3000, host: 3000
  end
  c.vm.define "vm2" do |vm2|
    c.vm.network "forwarded_port", guest: 3001, host: 3001
  end
end
