Role Name
=========

Installs Docker/ensures Docker is installed and operational

Requirements
------------
- APT 

Role Variables
--------------

- default_uname: the user to add to the Docker group, if any. Defaults to hoodn.

Dependencies
------------

- None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: hoodnoah.docker, default_uname: "hoodn" }

License
-------

- MIT

Author Information
------------------

