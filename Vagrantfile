Vagrant.configure("2") do |config|
  config.vm.provider "libvirt"
  config.vm.provider :libvirt do |domain|
     domain.qemu_use_session = false
  end
  config.vm.box = "fedora/35-cloud-base"
  config.vm.box_version = "35.20211026.0"
  config.vm.network "private_network", type: "dhcp"
end
