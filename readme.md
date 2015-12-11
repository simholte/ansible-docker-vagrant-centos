## Spring Boot Application inside of a Docker container Deployed with Ansible##

###Pre-reqs for Mac OSX###
1. brew cask install virtualbox
2. brew cask install vagrant
3. brew cask install vagrant-manager  *Vagrant-Manager helps you manage all your virtual machines in one place directly from the menubar.*
5. brew install Ansible



This is my first attempt at creating a simple Spring Boot application and putting it inside of a docker container, deployed using Ansible.

Next step is to scale the Spring Boot Application, then add service discovery and load balancing
To do that I used nginx as a reverse proxy load balance, https://consul.io/ as a service registry.  I also used registrator https://github.com/gliderlabs/registrator to monitor docker and perform the register action on Consul.  Another project Consul-Template https://github.com/hashicorp/consul-template ran on the lb, received signals from Consul and updated the lb config with any docker destroy or creation.

To run the application simply type
`vagrant up`

Once complete the following sites will be available: <br/>
The consul UI can be found  http://localhost:8500/ui/ <br/>
The Docker UI can be found http://localhost:9000/ <br/>
The actual SpringBoot Rest call can be executed by going to http://localhost:8080/ <br/>
