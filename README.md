ansible-role-macbook
=========

Ansible roles for MacOS to set some preferences and install packages. For example:

 - show filename extensions
 - enable Dark theme
 - disable `.DS_Store` file creation on network shares
 - install packages like `wget`, `screen` and `vlc`

Requirements
------------

 - [Homebrew package manager](https://brew.sh/) (for the `macbook-pkgs` role)

Role Variables
--------------

Set your required Homebrew packages and casks in `roles/macbook-pkgs/defaults/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

Inventory file:
    
    localhost ansible_connection=local

Playbook:

    ---
    - hosts: localhost
      roles:
        - macbook-prefs
        - macbook-pkgs

Run the playbook:

   ansible-playbook -i inventory site.yml 

You will need to reboot after running this playbook because OSX Defaults are cached.

License
-------

BSD
