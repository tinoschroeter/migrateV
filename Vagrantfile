Vagrant.configure("2") do |config|
config.vm.define "migrateV" do |migrateV|
  migrateV.vm.hostname = "migrateV"
  migrateV.vm.box = "ubuntu/xenial64"
  migrateV.vm.provision "file", source: "./migrate2vagrant", destination: "/tmp/migrate2vagrant"
  migrateV.vm.provision "shell", inline: "apt-get update;apt-get install -y rsync;mv /tmp/migrate2vagrant /usr/local/bin/migrate2vagrant"
  end
config.vm.provider "virtualbox" do |v|
  v.memory = 1024
  v.cpus = 2
  end
end
