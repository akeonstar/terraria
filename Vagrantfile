
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"

  config.vm.network "forwarded_port", guest: 7778, host: 7778

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  ## might just turn this into a dir once i get some more files
  config.vm.provision "file", source: "playbook.yml", destination: "/tmp/playbook.yml"
  config.vm.provision "file", source: "serverconfig.txt.j2", destination: "/tmp/serverconfig.txt.j2"


  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y ansible
    ansible-playbook /tmp/playbook.yml
  SHELL

end
