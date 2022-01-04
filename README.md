`Wordpress Role`
=========

A light role to install Wordporess on a remote host via docker. this role also install docker and all prerequistes `python-pip and docker-py` necessary to run a concaiter with the docker_container module 

Requirements
------------
Note that this  works only on Ubuntu or CentOS Linux distribution
Need to user `sadofrazer.docker_role` to install docker first

Role Variables
--------------

For this role we just have 02 variables which permit us to modify the name of the remote host if necessary:

  - `instance_name`: Name of the wordpress instance  (default : frazer) #use to prefix all the docker ressources, it can be replace by the company name if you prefer
  - `mysql_container`: the name of the mysql container (default : mysql)
  - `wordpress_container`: the name of the wordpress web container (default : wordpress)
  - `network_name`: the name of  the network in wich all containers are link (default : wp-network)
  - `volume_name`: the name of docker volume to save the BDD files (default : mysql-data)
  - `wp_port`: the port number to expose the wordpress app on host (default: 8085)
  - `mysql_port`: the port number to expose  mysql database if need to administarte it with a database administartor tool (default : 3306)
  - `mysql_image`: image tag or version of mysql to use (default: mysql)
  - `Wordpress_image`: image or version of wordpress to use (default: wordpress)
  - `db_name`: Name of the datababe (default: wp-db)
  - `db_user`: frazer
  - `db_password`: frazer
  - `db_root_password`: root

Dependencies
------------

Any dependency for this role.

Example Playbook
----------------

Find below an example of playbook to use this role:

    - hosts: servers
      vars:
        instance_name: test
      roles:
         - sadofrazer.docker_role
         - sadofrazer.wordpress_role

License
-------

NONE

Author Information
------------------

`Frazer SADO`.
