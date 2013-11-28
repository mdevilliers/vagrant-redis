Vagrant.configure("2") do |config|
  config.vm.box = "precise64"

  # THE URL FROM WHERE THE 'CONFIG.VM.BOX' BOX WILL BE FETCHED IF IT
  # DOESN'T ALREADY EXIST ON THE USER'S SYSTEM.
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.network :forwarded_port, guest: 6379, host: 6379

  # Set virtual machine memory size
  config.vm.provider :virtualbox do |vbox|
    vbox.customize ["modifyvm", :id, "--memory", 1024]
  end

  config.vm.provision :shell, :path => "init.sh"
end
