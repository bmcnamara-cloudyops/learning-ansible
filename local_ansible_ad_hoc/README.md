# Learning Ansible

This repository stores example code for the blog [Learning Ansible](https://www.learningansible.com).  Since Ansible is a Python project, a requirements.txt file has been included.  Combined with the pip Python package manager, users should be able to install all Python dependencies.  

Though technically not required, [I recommend installing the Python packages into a virtual environment using virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv).  Using a virtual environment allows projects to maintain different versions of Python modules without conflict.

## Installing Project Dependencies

Please see my Learning Ansible blog posts on [installing Vagrant and VirtualBox](https://learningansible.com/2017/10/17/working-with-ansible-locally-using-virtualbox-and-vagrant-part-1-of-2/) and [using Ansible locally](https://learningansible.com/2017/10/27/working-with-ansible-locally-using-virtualbox-and-vagrant-part-2-of-2/) for more detailed instructions on installing the prerequisites.

## Running ad-hoc Commands with Ansible

Ansible has the capability to act as an orchestrator, deploying configurations and managing services using a well defined set of primitives.  But sometimes one-off commands have to be run.  Is this user defined locally on a set of hosts?  I just need to know the kernel version for a list of hosts - can I just do something simple with Ansible?

Fortunately, the answer is yes.  Many of the simple things can be done in a complex manner.  But it is possible to write an ad-hoc command in place of something like [Fabric](http://www.fabfile.org/).  

I've included some examples for how we can run simple operating system commands using Ansible.  This list of examples is not exhaustive - it's only limited by what you can run on the operating system.  Take care, though.  If you find yourself doing anything _beyond_ a simple one-liner you should likely be looking at using a Ansible playbook.  

I'm giving you a hammer - remember that not everything is a nail.

## Getting Started

### Bring up the Virtual Machines

```
cd ansible
vagrant up
vagrant status # Should show two virtual machines: web and notweb
```
