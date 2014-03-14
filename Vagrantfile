Vagrant.configure("2") do |config|
  config.vm.box      = 'precise64'
  config.vm.box_url  = 'http://files.vagrantup.com/precise64.box'

  config.vm.hostname = 'clojure-dev'
  
  config.vm.network :private_network, ip: '33.33.33.33'

  config.vm.provision "ansible" do |ansible|
    ansible.playbook       = 'clojure/setup.yml'
    ansible.inventory_path = 'hosts'
    ansible.verbose        = 'vvv'
  end
  
  config.vm.provider :virtualbox do |vb|
    vb.customize ['modifyvm', :id, '--memory', 2048]
  end
end
