
Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/ubuntu2004"

  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

# VM configuration
  config.vm.define "ubuntu2004" do |ubuntu2004|
    ubuntu2004.vm.hostname = "ansible"
# Port forwarding configuration
    ubuntu2004.vm.network "forwarded_port", guest: 3000, host: 3000  
    ubuntu2004.vm.network "forwarded_port", guest: 5000, host: 5000  
  end

  config.vm.provision "ansible" do |ansible|
    ansible.compatibility_mode = "auto"
    ansible.playbook = "/Users/petergichana/Desktop/devopsmoringa/yolo/docker-playbook.yml"
  end
end
