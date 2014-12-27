packages
=========

Ansible role for installing any packages without it's configuration, for example: atop, htop, ethtool and so on. Additionally this role allows you to add repositories you want.

Requirements
------------

No requirements.

Role Variables
--------------

This role contains only two variables:

* packages_repositories - list of repositories you want to add. Subelemets are:

** url - url to repository key

** string - repository string (example: deb http://apt.domain.com/ wheezy main contrib non-free)


* packages_list - list of packages you want to install (htop, atop and so on)


Dependencies
------------

No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all 
      roles:
         - { role: vozerov.packages, packages_list: ['atop', 'htop'] }

License
-------

Apache
