# Docker (containerization) vs Vagrant (virtual machine)

- What if you can run an application on your machine, but someone on another machine can't?
- If you want to manage machines, you should use Vagrant. If you want to build and run applications environments, you should use Docker. Vagrant is a tool for managing virtual machines. Docker is a tool for building and deploying applications by packaging them into lightweight containers.

## Vagrant

![monolithic](../search_pics/Docker%20containerization%20vs%20Vagrant%20virtual%20machine/vagrant.png)

- Say you start with a fresh virtual machine, then you have a "provisioning script" which installs on the virtual machine all the extra software you need to run your application.
- This "provisioning script" is also run on the staging server (server for development/testing) and production server (server to publish finished application) so that anyone can inintialize a virtual machine and run your application.
- Now, someone can just take your project code from github and run your application from any virtual machine as long as they use the "provisioning script" to install everything.

## Docker

![monolithic](../search_pics/Docker%20containerization%20vs%20Vagrant%20virtual%20machine/docker.png)

- Docker uses a "dockerfile" to convert your project code and all installation requirements into a "docker image" (this image is essentially everything you need to run your application).
- You then run this "docker image" as something called a "container", and you can run as many of these "containers" as you want on a single virtual machine (as long as you don't run out of memory).
- You store your "docker image" on essentially a docker version of Github (like Docker Hub) and now any machine with Docker can run your applicatino using the "docker image".
- Amazon's "ECS" (EC2 (elastic compute cloud) Container Service) platform can manage your containers for you.