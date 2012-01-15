# Jenkins Server

This project sets up [Jenkins] using [Vagrant] and [Chef]. It serves as my
first experiment with Jenkins, Vagrant, or Chef.

[Jenkins]: http://jenkins-ci.org/
[Vagrant]: http://vagrantup.com/
[Chef]: http://www.opscode.com/chef/

## Setup

This assumes some version of Ruby and [VirtualBox] are installed. Download and install VirtualBox from [its website][VirtualBox].

```shell
    bundle install # to install the vagrant and chef gems
    vagrant box add base http://files.vagrantup.com/lucid32.box # to download a base ubuntu virtual machine image
    vagrant up # to set up the virtual machine with the vagrant configuration and chef recipes in the project
```

Now the server should be running. Stop it with `vagrant halt` or SSH into the server to inspect it with `vagrant ssh`.

[VirtualBox]: https://www.virtualbox.org/wiki/Downloads


## What Are These Tools?

Jenkins is a continuous-integration server, which we plan to use to automatically run test as developers commit code.

Vagrant is a tool to distribute virtual machine configuration.

Chef is used by Vagrant to automate the setup of these virtual machines.
