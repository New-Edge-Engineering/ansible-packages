# Packages [![Build Status](https://travis-ci.com/New-Edge-Engineering/ansible-packages.svg?branch=master)](https://travis-ci.org/New-Edge-Engineering/ansible-packages)

Ansible role for installing any packages without it's configuration, for example: atop, htop, ethtool and so on. Additionally this role allows you to add repositories you want.

## Requirements

No requirements.

## Role Variables

This role contains only two variables:

* packages_repositories - list of repositories you want to add. Supported by Yum and APT with different Attributes.
  * APT (one of the following):
    * key - url to repository key
    * url - url to repository.
  * Yum:
    * name - The name of the package repository.
    * description - Optional description.
    * baseurl - Optional URL for the package repository base
    * mirrorlist - Optional URL for the package repository list of mirrors
    * enabled - Optional activation of the package repository (defaults to yes).
    * gpgcheck - Optional gpg check of the package repository (defaults to no).
    * state - Optional state override (defaults to present).
* packages - list of packages you want to install (ntp, htop, atop and so on)

## Dependencies

No dependencies.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all 
      roles:
         - { role: neel.packages, packages: ['atop', 'htop'] }

See the molecule tests for more.

## License

Apache

## Contributing

* Follow step one in [How To Test Ansible Roles with Molecule](https://www.digitalocean.com/community/tutorials/how-to-test-ansible-roles-with-molecule-on-ubuntu-18-04) to set up environment.
* Please submit Pull Request via github.
