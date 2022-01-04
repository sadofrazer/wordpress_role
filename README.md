Docker Role
=========

A light role to install docker on a remote host and also install all prerequistes `python-pip and docker-py` necessary to run a concaiter with the docker_container module 

Requirements
------------
This role has any prerequistes, it can works just on Ubuntu or CentOS Linux distribution

Role Variables
--------------

For this role we just have 02 variables which permit us to modify the name of the remote host if necessary:

  - `edit_hostname`: yes/no (default : yes) #to specify if you also want change the hostname
  - `hostname`: the new hostname (default : AnsibleWorker)

Dependencies
------------

Any dependency for this role.

Example Playbook
----------------

Find below an example of playbook to use this role:

    - hosts: servers
      vars:
        edit_hostname: no
      roles:
         - role: sadofrazer.docker_role

License
-------

NONE

Author Information
------------------

`Frazer SADO`.
