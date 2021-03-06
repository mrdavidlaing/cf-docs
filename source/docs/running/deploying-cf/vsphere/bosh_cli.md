# BOSH CLI #

BOSH CLI is a command line interface used to interact with MicroBOSH and BOSH. 
Before we can use MicroBOSH or BOSH we need to install BOSH Command Line Interface.

## Installing BOSH Command Line Interface ##

The following steps install BOSH CLI on Ubuntu 12.04.1 LTS. You can install on either a physical or Virtual Machine.

### Install Ruby ###

Ruby can be installed using either rbenv or rvm. Please refer to the following documents for more details

1. [Install ruby using rvm](../common/install_ruby_rvm.html)
2. [Install ruby using rbenv](../common/install_ruby_rbenv.html)


### Install Local BOSH and BOSH Releases ###

1. Sign up for the Cloud Foundry Gerrit server at [http://reviews.cloudfoundry.org](http://reviews.cloudfoundry.org)

1. Set up your ssh public key (accept all defaults)

		ssh-keygen -t rsa

1. Copy your key from `~/.ssh/id_rsa.pub` into your Gerrit account

1. Create and upload your public SSH key in your Gerrit account profile

1. Set your name and email

		git config --global user.name "Firstname Lastname"
		git config --global user.email "your_email@youremail.com"

1. Install gerrit-cli gem

		gem install gerrit-cli

1. Run some rake tasks to install the BOSH CLI

		gem install bosh_cli
	
_Note : run `rbenv rehash`command if you used rbenv to install ruby_
		
		bosh --version


