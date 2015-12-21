# sling-docker-nosql
Test for Sling in docker using nosql 

This project will use fig to produce four docker container.
A nginx frontend as a load balancer for two sling instances.
Two sling instances using oak and a mongo-repository.
A mongodb instance serving the reposotory data of the sling containers.
This is a pure testing and gambling environment. It´s not made for production.


##Prerequisites
A provider for vagrant. I use VirtualBox.(https://www.virtualbox.org/)
Vagrant itself. (https://www.vagrantup.com/)

##Running
After cloning this repo, just run `vagant up`.
Open a shell in the created vm using `vargant ssh`.
Change to /vagrant/container/fig-sling-db and run `fig up`.
After some tome and some download the containers should run. 
You could now open http://192.168.100.20 to see the page delivered by nginx.
The URLs http://192.168.100.20:8080 and http://192.168.100.20:8081 are the the pages of the two sling instances. 


The very first start seems to create a race condition. Both sling instances are trying to create the mongo-store. 
One winns - one dies.  Next start will run both instances. More on this later.  

Any comments would be highly appreciated.

