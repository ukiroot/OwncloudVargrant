Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.ssh.insert_key = false
  config.vm.network "forwarded_port", guest: 80, host: 8087
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end
