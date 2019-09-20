Vagrant.configure("2") do |config|
    config.vm.box = "fedora/31-cloud-base"
    config.vm.box_version = "31.20191023.0"
    config.vm.network "forwarded_port", guest: 443, host: 8443
    config.vm.provider "libvirt" do |vb|
      vb.random :model => 'random'
      vb.memory = "2048"
      vb.cpus = "2"
   end
   config.vm.provision "ansible_local" do |ansible|
     ansible.playbook = "playbook.yml"
     ansible.compatibility_mode = "2.0"
  end
end
