Jira standalone
===============

CentOS 7 based Jira server.

## requirements

* the centos base image (CentOS 6.8 x64 from https://github.com/box-cutter/centos-vm)
* Ansible 2.x on your host machine


## setting things up

Run the play with:

    ansible-playbook -i meta/ site.yml

this will install Jira and a local mysql DB for it to use.

Jira doesn't make it easy to automate itself; so although we create
a DB and user you have to connect Jira to it yourself.

At the end of the play, ansible will output a message with what
you need to manually enter into the Jira UI.

You can also upload/create a license key, etc.


