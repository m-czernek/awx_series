# Getting started with Ansible Tower
The following repository serves as hands-on lab for getting started with 
[Ansible Tower](https://www.ansible.com/products/tower). Because 
Tower is paid software distributed by Red Hat, this tutorial uses the
open-source upstream on which Tower was build, the 
[AWX](https://www.ansible.com/products/awx-project) project.

## Prerequisites

The lab uses a couple of programs:

* Ansible
* Vagrant

Make sure you installed both before proceeding with the lab.

## Recommended training

Ansible Tower is used for advanced Ansible automation. Consequently,
without knowledge of Ansible, Tower is not very useful. 

Red Hat provides a free training for Ansible, 
[DO007](https://www.redhat.com/en/services/training/do007-ansible-essentials-simplicity-automation-technical-overview).
If you are not familiar with Ansible, I'd recommend you complete the 
above-mentioned course.

## Start hacking

To start with Ansible Tower, or AWX, change into the first directory and 
follow the README.md: `cd 01_provision`. 

## Troubleshooting

### Vagrant virtualization provider
The Vagrantfile definitions provided in this repository use the `libvirt`
provider. This is the default Vagrant provider if you install Vagrant
on Fedora using the `dnf` package manager.

If you are running a different operating system, please change the 
Vagrantfile VM provider to whatever provider you have available.
For example:

```
c.vm.provider :libvirt do |libvirt|
```

should be changed to:

```
c.vm.provider "virtualbox" do |libvirt|
```

for each VM.
