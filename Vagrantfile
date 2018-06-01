# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'yaml'
settings = YAML.load_file 'settings.yml'

git_home = settings['git_home'] || ENV['GIT_HOME']

Vagrant.configure("2") do |config|  
  config.vm.box = "cjvirtucio87/vmware-centos7"
  config.vm.box_url = "file:///#{git_home}/cjvirtucio87-infra/packer/builds/vmware-centos7.box"
  config.vm.synced_folder ".", "/mnt/hgfs", type: "rsync"
  config.ssh.insert_key = false
end
