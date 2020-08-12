Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provision "file", source: "provisioning/static-site-src", destination: "/tmp/static-site-src"

  config.vm.provision "shell", inline: "mv /tmp/static-site-src/* /usr/share/nginx/html/static-site-src"

  # Run Ansible from Vagrant VM
  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.verbose = "v"
    ansible.playbook = "provisioning/site.yml"
    config.vm.network :forwarded_port, guest: 80, host: 4567
  end
end
