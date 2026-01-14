Vagrant.configure("2") do |config|
 config.vm.box = "debian/bullseye64"

  config.vm.network "private_network", ip: "192.168.7.5"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.synced_folder ".", "/vagrant"
end