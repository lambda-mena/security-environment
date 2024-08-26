Vagrant.configure("2") do |config|
  config.vm.define :kali do |kali|
    kali.vm.box = "kalilinux/rolling"
    kali.vm.network :private_network, ip: "192.168.50.3"
    kali.vm.hostname = "kali"
  end

  config.vm.define :victim do |victim|
    victim.vm.box = "rapid7/metasploitable3-ub1404"
    victim.vm.box_version = "0.1.12-weekly"
    victim.vm.network :private_network, ip: "192.168.50.2"
    victim.vm.hostname = "victim"
    victim.ssh.username = "vagrant"
    victim.ssh.password = "vagrant"
  end
end
