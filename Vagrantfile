# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/yakkety64' # 16.10
  config.vm.hostname = 'rails-dev-box'

  config.vm.network :forwarded_port, guest: 1234, host: 1234

  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true

  config.vm.provider 'virtualbox' do |v|
    v.memory = 2048
    v.cpus = 2
    v.gui = false 
  end
end
