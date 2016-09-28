# Digital Ocean Packer Template to build Hugo based blog for SexySexyPenguins.com

This repo provides the basic Packer Template, Ansible Playbooks and
configurations for creating a [Hugo](http://gohugo.io)-based blog, running on CentOS 7.3.
The build becomes a snapshot image on Digital Ocean.

This repository is structured as such:

    centos/
    ├── ansible # ansible configurations used by Packer
    │   ├── group_vars # global variables
    │   │   └── all # vars for all hosts (only one in this case)
    │   ├── roles
    │   │   ├── common # any common tasks that need to be performed
    │   │   ├── hugo # tasks to build hugo
    │   │   ├── nginx # tasks to build an nginx to host static hugo pages
    │   └── setup.yml # playbook to call the above tasks
    └── DO-centos-7.3-blog-server-x86_64.json # packer build configuration


