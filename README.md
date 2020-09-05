Ansible basic server
=========

Role to setup a basic server with ansible.
The role does the following:

* Setup APT apt_keys
* Setup APT proxy
* Setup APT source.list
* Update and upgrade apt
* Install default programs I like.
* Raspbian:

  - Wifi, set country
  - Zram Setup
  - Remove SWAP
  - Remove the user 'pi'
  - Set boot settings
  - remove warning MOTD
  - modify rasp-config to my liking, to enable powersave.
 
Requirements
------------

* None

Role Variables
--------------

Tested OS
---------

* Rasbian (Raspberry PI)
* Ubuntu


Dependencies
------------

- None

Example Playbook
----------------
````
- hosts: debian
  become: true

  roles:
  - basic-server

  vars:
     apt_proxy: "192.168.2.8:3142"
````
License
-------

GPL-2.0-or-later

Author Information
------------------

role author: Torstein Eide
git-repository:
