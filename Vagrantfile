
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"

  config.vm.network "forwarded_port", guest: 7777, host: 7777

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  ## might just turn this into a dir once i get some more files
  config.vm.synced_folder "ansible/", "/opt/ansible"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y ansible
    cd /opt/ansible/
    ansible-playbook playbook.yml
  SHELL

end
