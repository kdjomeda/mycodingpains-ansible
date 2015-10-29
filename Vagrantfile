Vagrant.configure("2") do |config|
    auto_config= false

   config.vm.provider "virtualbox" do |v|
       v.gui = true
   end

   config.vm.define "app1" do |app1|
          app1.vm.box = "ubuntu/trusty64"
          app1.vm.network "private_network" , ip:"192.168.56.163", :adapter =>2
   end

   config.vm.define "app2" do |app2|
          app2.vm.box = "ubuntu/trusty64"
          app2.vm.network "private_network" , ip:"192.168.56.164", :adapter =>2
   end


     config.vm.define "db" do |db|
        db.vm.box = "ubuntu/trusty64"
        db.vm.network  "private_network" , ip:"192.168.56.165", :adapter =>2
        db.vm.provider "virtualbox" do |vb|
           vb.memory = "1024"
        end

   end


end
