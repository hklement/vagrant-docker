VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu/trusty64'

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network 'private_network', ip: '192.168.23.75'

  # Install and configure Docker.
  config.vm.provision :shell, path: 'docker.sh'

  # Share an additional folder to the guest VM.
  config.vm.synced_folder '/shared', '/shared'
end
