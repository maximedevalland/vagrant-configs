How Vagrant works ?
-------------------
Vagrant is like an enhanced command line interface for VirtualBox.
You have a vagrant directory for each of your VMs containing a configuration File. You will need to run all your vagrant commands from this directory.
The magic happens when you use chef-client in your Vagrantfile to install packages automatically in your VM.

Make sure you have installed Virtualbox : https://www.virtualbox.org/wiki/Downloads

Installation
------------

* Download Vagrant from
https://www.vagrantup.com/downloads.html
* Create a vagrant directory where you want to put your Vagrant configs
```
mkdir ~/vagrant
```
* Create a directory specific for a VM, for ex : 
```
mkdir ~/vagrant/chef-server
```
* Initialize vagrant in its directory
```
cd ~/vagrant/chef-server
vagrant init
```
* Add a box locally, here "precise32", choose from : https://vagrantcloud.com/discover/featured OR http://www.vagrantbox.es/
```
vagrant box add precise32 http://files.vagrantup.com/precise32.box
```

* Edit Vagrantfile according to your expections. See https://github.com/MaximeDevLA/vagrant-configs/Vagrantfiles
* Start vagrant, it will spin up your new VM. Same command to start the VM if it was shutdown. It's not gonna re-install the VM though.
```
vagrant up
```
