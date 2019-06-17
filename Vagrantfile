Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/xenial64"
   config.vm.network "private_network", ip: "192.168.56.10"
	config.vm.host_name = "ckan.local"
	config.vm.provider "virtualbox" do |vb|
		 vb.name = "louisvilledatacommons"
	    vb.customize ["modifyvm", :id, "--memory", "2048"]
	    vb.customize ["modifyvm", :id, "--cpus", "2"]  
    end
    
	config.vm.provision :shell, path: "bootstrap_280.sh"
	#config.vm.synced_folder "../ckanext-ifel", "/home/vagrant/sciamlab-ckan/src/ckanext-ifel"
	
end
