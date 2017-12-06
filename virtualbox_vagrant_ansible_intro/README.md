# Learning Ansible

This repository stores example code for the blog [Learning Ansible](https://www.learningansible.com).  Since Ansible is a Python project, a requirements.txt file has been included.  Combined with the pip Python package manager, users should be able to install all Python dependencies.  

Though technically not required, [I recommend installing the Python packages into a virtual environment using virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv).  Using a virtual environment allows projects to maintain different versions of Python modules without conflict.

## Installing Project Dependencies

I've created a single video that outlines how to install VirtualBox and Vagrant.  [It is available on YouTube](https://www.youtube.com/watch?v=WnZI-KLUan0).

### Installing Python Packages

```
pip install -r requirements.txt
```

### Installing VirtualBox

[VirtualBox installation details](https://www.virtualbox.org/manual/ch02.html)

### Installing Vagrant

[Installing Vagrant](https://www.vagrantup.com/docs/installation/)

## Managing Virtual Machines with Vagrant

Vagrant has a rich command-line interface (CLI) that allows for management of virtual machines.  I've listed several subcommands that are commonly used with vagrant.  For a more thorough reference please consult [the CLI docs](https://www.vagrantup.com/docs/cli/)

```
vagrant status      # Print out the status of a virtual machine
vagrant up          # Bring up a virtual machine
vagrant halt        # Bring down a virtual machine
vagrant reload      # Perform a vagrant halt followed by a vagrant up
vagrant destroy     # Stop the virtual machine and destroy all resources created during the creation process
vagrant provision   # Run provisioner(s) defined in the Vagrantfile
vagrant ssh         # Connect to the virtual machine via command-line
vagrant ssh-config  # Display the SSH configuration of the virtual machine
```

In our case, the virtual machine `default` can be provisioned and configured by running the following command:

```
vagrant up default
```
