# Simple Node.js Development VM

This project aims to make spinning up a simple local Node.js test/development environment incredibly quick and easy, and to introduce new developers to the wonderful world of Node.js development on local virtual machines.

It will install the following on a CentOS 6.4 linux VM:

  - Node.js (latest version in EPEL repository)
  - Express
  - A simple demonstration Node.js app

It should take 5-10 minutes to build or rebuild the VM from scratch on a decent broadband connection.

## Quick Start Guide

### 1 - Install dependencies (VirtualBox, Vagrant, Ansible)

  1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  2. Download and install [Vagrant](http://www.vagrantup.com/downloads.html).
  3. [Mac/Linux only] Install [Ansible](http://docs.ansible.com/intro_installation.html).

Note for Windows users: *This guide assumes you're on a Mac or Linux host. Windows support may be added when I get a little more time; the main difference is Ansible needs to be bootstrapped from within the VM after it's created. See [JJG-Ansible-Windows](https://github.com/geerlingguy/JJG-Ansible-Windows) for more information.*

### 2 - Build the Virtual Machine

  1. Download this project and put it wherever you want.
  2. Open Terminal, cd to this directory (containing the `Vagrantfile` and this REAMDE file).
  3. Type in `vagrant up`, and let Vagrant do its magic.

Note: *If there are any errors during the course of running `vagrant up`, and it drops you back to your command prompt, just run `vagrant provision` to continue building the VM from where you left off. If there are still errors after doing this a few times, post an issue to this project's issue queue on GitHub with the error.*

### 3 - Configure your host machine to access the VM.

  1. [Edit your hosts file](http://www.rackspace.com/knowledge_center/article/how-do-i-modify-my-hosts-file), adding the line `192.168.55.55  nodejs.dev` so you can connect to the VM.
  2. Open your browser and access [http://nodejs.dev/](http://nodejs.dev/).

## Notes

  - To shut down the virtual machine, enter `vagrant halt` in the Terminal in the same folder that has the `Vagrantfile`. To destroy it completely (if you want to save a little disk space, or want to rebuild it from scratch with `vagrant up` again), type in `vagrant destroy`.
  - Find out more about local development with Vagrant + VirtualBox + Ansible in this presentation: [Local Development Environments - Vagrant, VirtualBox and Ansible](http://www.slideshare.net/geerlingguy/local-development-on-virtual-machines-vagrant-virtualbox-and-ansible).
  - Learn about how Ansible can accelerate your ability to innovate and manage your infrastructure by reading [Ansible for DevOps](http://www.ansiblefordevops.com/).

## About the Author

[Jeff Geerling](http://jeffgeerling.com/) created this project in 2014 for easier local Node.js development. This project, and others like it, are also featured as examples in Jeff's book, [Ansible for DevOps](http://www.ansiblefordevops.com/).
