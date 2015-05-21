# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "machine1" do |machine1|
    machine1.vm.box = "precise32"
    machine1.vm.box_url = "http://files.vagrantup.com/precise32.box"

    machine1.vm.network :public_network
  end

  config.vm.define "machine2" do |machine2|
    machine2.vm.box = "precise32"
    machine2.vm.box_url = "http://files.vagrantup.com/precise32.box"

    machine2.vm.network :public_network
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant.yml"
    ansible.inventory_path = "inventory/vagrant"
  end
end
