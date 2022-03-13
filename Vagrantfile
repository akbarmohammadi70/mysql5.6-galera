Vagrant.configure("2") do |config|
  config.vm.define "maxscale1" do |maxscale1|
    maxscale1.vm.box = "ubuntu/focal64"
    maxscale1.vm.hostname = 'maxscale1'
    maxscale1.vm.box_url = "ubuntu/focal64"

    maxscale1.vm.network :private_network, ip: "192.168.56.101"
    
  config.vm.provision "shell" do |s|
    ssh_pub_key = File.readlines("/home/vagrant/.ssh/id_rsa.pub").first.strip
    s.inline = <<-SHELL
      echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
      echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
    SHELL
  

    maxscale1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "maxscale1"]
    end
  end
 end
  config.vm.define "maxscale2" do |maxscale2|
    maxscale2.vm.box = "ubuntu/focal64"
    maxscale2.vm.hostname = 'maxscale2'
    maxscale2.vm.box_url = "ubuntu/focal64"

    maxscale2.vm.network :private_network, ip: "192.168.56.102"

  config.vm.provision "shell" do |s|
    ssh_pub_key = File.readlines("/home/vagrant/.ssh/id_rsa.pub").first.strip
    s.inline = <<-SHELL
      echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
      echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
    SHELL
 

    maxscale2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "maxscale2"]
    end
  end
 end
   config.vm.define "db1" do |db1|
    db1.vm.box = "ubuntu/bionic64"
    db1.vm.hostname = 'db1'
    db1.vm.box_url = "ubuntu/bionic64"

    db1.vm.network :private_network, ip: "192.168.56.103"

  config.vm.provision "shell" do |s|
    ssh_pub_key = File.readlines("/home/vagrant/.ssh/id_rsa.pub").first.strip
    s.inline = <<-SHELL
      echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
      echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
    SHELL
  

    db1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "db1"]
    end
  end
 end

   config.vm.define "db2" do |db2|
    db2.vm.box = "ubuntu/bionic64"
    db2.vm.hostname = 'db2'
    db2.vm.box_url = "ubuntu/bionic64"

    db2.vm.network :private_network, ip: "192.168.56.104"

  config.vm.provision "shell" do |s|
    ssh_pub_key = File.readlines("/home/vagrant/.ssh/id_rsa.pub").first.strip
    s.inline = <<-SHELL
      echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
      echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
    SHELL
      

    db2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "db2"]
    end
  end
 end

  config.vm.define "db3" do |db3|
    db3.vm.box = "ubuntu/bionic64"
    db3.vm.hostname = 'db3'
    db3.vm.box_url = "ubuntu/bionic64"

    db3.vm.network :private_network, ip: "192.168.56.105"
   
    config.vm.provision "shell" do |s|
    ssh_pub_key = File.readlines("/home/vagrant/.ssh/id_rsa.pub").first.strip
    s.inline = <<-SHELL
      echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
      echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
    SHELL
  

    db3.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "db3"]
    end
  end
 end


end


