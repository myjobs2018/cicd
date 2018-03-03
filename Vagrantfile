Vagrant.configure(2) do |config|
  config.ssh.private_key_path = "~/.ssh/id_rsa"
#  config.ssh.private_key_path = "~/.ssh/authorized_keys"
  config.vm.boot_timeout = 500
  config.ssh.forward_agent = true
  config.ssh.insert_key=false
#  config.vm.provider "virtualbox" do |vb|
#    vb.gui = true
#    vb.memory = "2048"
#  end
 config.vm.define "webserver" do |webserver|
  webserver.vm.box = "ubuntu/trusty64"
  webserver.vm.network "private_network", ip: "192.164.0.2"
  webserver.vm.hostname = "webserver"
 end
 config.vm.define "ansible" do |ansible|
  ansible.vm.box = "ubunty/trusty64"
  ansible.vm.network "private_network", ip: "192.164.0.254"
  ansible.vm.hostname = "ansible"
 end
end
