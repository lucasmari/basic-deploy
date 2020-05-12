Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"
  
# Run Ansible from the Vagrant VM
  config.vm.provision "ansible" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.verbose = "v"
    ansible.playbook = "provisioning/site.yml"
    config.vm.network :forwarded_port, guest: 80, host: 4567
  end
end
