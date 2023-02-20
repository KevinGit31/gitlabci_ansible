Vagrant.configure("2") do |config|

	config.vm.define "vmdockergitlabgitlab" do |vmdockergitlab|
		vmdockergitlab.vm.hostname = 'vmdockergitlab'
		vmdockergitlab.vm.box = "ubuntu/bionic64"
		#vmdockergitlab.disksize.size = '15GB'
		vmdockergitlab.vm.provider "virtualbox" do |vb|
			vb.memory = 6000
			vb.cpus = 3
			vb.name = "vmdockergitlab"
			vb.gui = false
		end
		vmdockergitlab.vm.network "private_network", ip: "172.30.1.81"
		vmdockergitlab.vm.synced_folder "project/", "/home/project", create: true
		# Provisioning
		vmdockergitlab.vm.provision :shell, :path => "install_docker.sh"
	end

end
