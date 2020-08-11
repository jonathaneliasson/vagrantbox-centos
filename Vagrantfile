# This guide is optimized for Vagrant 1.8 and above.
# Older versions of Vagrant put less info in the inventory they generate.
Vagrant.require_version ">= 1.8.0"

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"

  config.vm.synced_folder "/Users/jonathan.eliasson/internetstiftelsen/", "/home/vagrant/internetstiftelsen/"
  config.vm.synced_folder "/Users/jonathan.eliasson/ansible/", "/home/vagrant/ansible/"
  config.vm.synced_folder "/Users/jonathan.eliasson/docker/", "/home/vagrant/docker/"
  config.vm.synced_folder "/Users/jonathan.eliasson/github/", "/home/vagrant/github/"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end
