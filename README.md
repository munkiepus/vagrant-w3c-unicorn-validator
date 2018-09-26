# Vagrant W3C build [![Build Status](https://travis-ci.org/munkiepus/vagrant-w3c-unicorn-validator.svg?branch=master)](https://travis-ci.org/munkiepus/vagrant-w3c-unicorn-validator)

Run latest Jenkins instance on Ubuntu 18.04 LTS using vagrant.

## Prerequisites
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

vagrant reload plugin
```
vagrant plugin install vagrant-reload
```

## Installation
Clone the repo
```
git clone git@github.com:munkiepus/vagrant-w3c-unicorn-validator.git
cd /vagrant-w3c-unicorn-validator
```

Build the vagrant box
```
vagrant up
```

To access the validator

```
http://localhost:8080
```

or, add the following line to the hosts file

```
127.0.0.1   validator.local
```

and then run the server with

```
http://validator.local:8080
```
