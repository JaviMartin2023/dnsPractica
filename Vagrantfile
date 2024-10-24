
Vagrant.configure("2") do |config|

  # Máquina 1: Linux gráfico (mercurio.sistema.test-----IMAGINARIA
  # Máquina 2: Debian texto (venus.sistema.test)
    config.vm.define "venus" do |venus|
      venus.vm.box = "debian/buster64"
      venus.vm.hostname = "venus.sistema.test"
      venus.vm.network "private_network", ip: "192.168.57.102"
      venus.vm.provider "virtualbox" do |vb|
        vb.name = "venus"
      end
      venus.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y bind9 bind9utils bind9-doc
    SHELL

    end

    # Máquina 3: Debian texto (tierra.sistema.test)
    config.vm.define "tierra" do |tierra|
      tierra.vm.box = "debian/buster64"
      tierra.vm.hostname = "tierra.sistema.test"
      tierra.vm.network "private_network", ip: "192.168.57.103"
      tierra.vm.provider "virtualbox" do |vb|
        vb.name = "tierra"
      end
      tierra.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y bind9 bind9utils bind9-doc
      SHELL
    end
    
    # Máquina 4: Windows gráfico o server (marte.sistema.test)-----IMAGINARIA
end
