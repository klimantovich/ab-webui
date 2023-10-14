Vagrant.configure("2") do |config|

  config.vm.define "webui" do |webui|
    webui.vm.box = "ubuntu/focal64"
    webui.vm.hostname = "webui.vm"
    webui.vm.network "private_network", ip: "10.0.5.13"

    webui.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
    end

    webui.vm.provision :ansible do |ansible|
      ansible.playbook = "./webui_setup.yml"
    end

  end

end

