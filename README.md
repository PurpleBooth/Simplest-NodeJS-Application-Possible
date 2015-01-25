# Simplest-Silex-Application-Possible
Simplest Silex application possible, with a vagrant box to run it for demo code.

## Dependencies

The following software needs to be installed
* [Vagrant](www.vagrantup.com)
* [Virtual Box](www.virtualbox.org)
* [Vagrant Hosts Manager Plugin](https://github.com/smdahlen/vagrant-hostmanager)

## Setup
Start the VM
```
vagrant up
```
Login to the VM
```
vagrant ssh
```
When on the VM install [Express](http://expressjs.com/) and it's dependencies
```
cd /vagrant
npm install
```
Then start the express server
```
npm start
```

Then hit the endpoint, from the your host machine, or the guest VM.
```
wget -O- http://00-express-node-npm:3000/
```
