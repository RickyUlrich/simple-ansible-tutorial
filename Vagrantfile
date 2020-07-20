

Vagrant.configure("2") do |config|
  # config.vm.box = "bento/ubuntu-18.04"
  # config.vm.box = "bento/ubuntu-16.04"
  # config.vm.box = "bento/debian-9.5"
  # config.vm.box = "bento/centos-6.9"
  config.vm.box = "bento/centos-7.5"
  # config.vm.box = "plus3it/spel-minimal-centos-6.9"
  # config.vm.box = "plus3it/spel-minimal-centos-7"

  config.vm.provider "virtualbox" do |v|
    v.memory = 6000
    v.cpus = 4
  end

  # this ansible play book is for deployment of standalone to another system
  # to use this role run: ansible-galaxy install -r requirements.yml
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.become = true
    ansible.playbook = "ansible-tutorial.yml"
  end

end
