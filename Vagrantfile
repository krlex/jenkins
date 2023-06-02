Vagrant.configure('2') do |config|
  config.vm.box = 'ubuntu/jammy64'
  config.vm.network 'forwarded_port', guest: 8090, host: 8090
  config.vm.network 'private_network', ip: '192.168.50.4'

  config.vm.provider 'virtualbox' do |vb|
    vb.gui = false
    vb.cpus = 2
    vb.memory = '2048'
  end

  config.vm.provision 'shell' do |shell|
    shell.path = 'bin/install.sh'
  end
end
