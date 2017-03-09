# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_API = 2
VAGRANT_WP_DOMAIN_NAME = ENV['VAGRANT_WP_DOMAIN_NAME'] || "example.site"
VAGRANT_WP_PASS = ENV['VAGRANT_WP_PASS'] || "vagrant"
VAGRANT_WP_SITE_TITLE = ENV['VAGRANT_WP_SITE_TITLE'] || "Example Site"
VAGRANT_WP_USER = ENV['VAGRANT_WP_USER'] || "webmaster"

Vagrant.configure(VAGRANT_API) do |config|

    config.vm.box = "ubuntu/trusty64"
    config.vm.network "forwarded_port", guest: 80, host:8080
    config.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
    config.vm.provision "shell", path: "deploy/vagrant.sh", args: [VAGRANT_WP_DOMAIN_NAME, VAGRANT_WP_SITE_TITLE, VAGRANT_WP_USER, VAGRANT_WP_PASS]

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
    end

end
