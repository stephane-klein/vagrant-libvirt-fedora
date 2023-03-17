Vagrant.configure("2") do |config|
  config.vm.provider "libvirt"
  config.vm.provider :libvirt do |domain|
     domain.qemu_use_session = false
  end
  config.vm.box = "generic/ubuntu2210"
  # config.vm.box = "fedora/35-cloud-base"
  config.vm.network "private_network", type: "dhcp"
end
