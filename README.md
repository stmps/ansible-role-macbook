ansible-role-macbook
=========

An Ansible role for setting some Mac OS preferences. For example:

 - showing filename extensions
 - enabling Dark theme
 - disabling `.DS_Store` file creation on network shares

Requirements
------------

 - [Homebrew package manager](https://brew.sh/)

Role Variables
--------------

Set your required Homebrew packages and casks in `defaults/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

Inventory file:
    
    localhost ansible_connection=local

Playbook:

    - hosts: localhost 
      roles:
         - ansible-role-macbook

Run the playbook:

   ansible-playbook -i inventory site.yml 

You will need to reboot after running this playbook because OSX Defaults are cached.

License
-------

BSD
