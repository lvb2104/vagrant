Vagrant.configure("2") do |config|
  config.vm.define "vm1" do |vm1|
    vm1.vm.provider "virtualbox" do |vb_vm1|
      vb_vm1.name = "server-1"
      vb_vm1.memory = "3072"
      vb_vm1.cpus = 2
      vb_vm1.gui = false
    end

    vm1.vm.box = "hashicorp-education/ubuntu-24-04"
    vm1.vm.network "private_network", ip: "192.168.56.11" # NAT network
    # vm1.vm.network "public_network", bridge: "wlp0s20f3: Wi-Fi (AirPort)", ip: "192.168.56.111"
    vm1.vm.hostname = "k8s-master-1"
  end

  config.vm.define "vm2" do |vm2|
    vm2.vm.provider "virtualbox" do |vb_vm2|
      vb_vm2.name = "server-2"
      vb_vm2.memory = "3072"
      vb_vm2.cpus = 2
      vb_vm2.gui = false
    end

    vm2.vm.box = "hashicorp-education/ubuntu-24-04"
    vm2.vm.network "private_network", ip: "192.168.56.12"
    vm2.vm.hostname = "k8s-master-2"
  end

  config.vm.define "vm3" do |vm3|
    vm3.vm.provider "virtualbox" do |vb_vm3|
      vb_vm3.name = "server-3"
      vb_vm3.memory = "3072"
      vb_vm3.cpus = 2
      vb_vm3.gui = false
    end

    vm3.vm.box = "hashicorp-education/ubuntu-24-04"
    vm3.vm.network "private_network", ip: "192.168.56.13"
    vm3.vm.hostname = "k8s-master-3"
  end

  config.vm.define "vm4" do |vm4|
    vm4.vm.provider "virtualbox" do |vb_vm4|
      vb_vm4.name = "server-4"
      vb_vm4.memory = "3072"
      vb_vm4.cpus = 1
      vb_vm4.gui = false
    end

    vm4.vm.box = "hashicorp-education/ubuntu-24-04"
    vm4.vm.network "private_network", ip: "192.168.56.14"
    vm4.vm.hostname = "rancher-server"
  end
end
