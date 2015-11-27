## Spring Boot Application inside of a Docker container##

###Pre-reqs for Mac OSX###
1. brew cask install virtualbox
2. brew cask install vagrant
3. brew cask install vagrant-manager  *Vagrant-Manager helps you manage all your virtual machines in one place directly from the menubar.*
5. brew install ansible



This is my first attempt at creating a simple Spring Boot application and putting it inside of a docker container.

Next step is to scale the Spring Boot Application, then add service discovery and load balancing

To run the application simply type
`vagrant up`