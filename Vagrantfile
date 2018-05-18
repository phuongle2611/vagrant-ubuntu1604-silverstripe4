Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.hostname = "vagrant"
  config.vm.network "public_network", ip: "192.168.12.153"
  config.vm.synced_folder ".", "/vagrant",
    owner: "www-data",
    group: "www-data",
    mount_options: ["dmode=777,fmode=777"]
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4048"
    vb.name = "vagrant"
  end
  config.vm.provision "shell", path: "setup/always.sh", run: "always"
end
