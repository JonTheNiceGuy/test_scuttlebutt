Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.box_check_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "public_network"

  config.vm.provision :ansible_local do |ansible|
    ansible.playbook       = "install_with_ansible.yml"
    ansible.install_mode   = "pip"
  end
end
