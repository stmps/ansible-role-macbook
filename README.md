ansible-role-macbook
=========

Ansible roles for macOS to set some preferences and install packages. For example:

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
Set your preferences in `roles/macbook-prefs/defaults/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

Inventory file: Refer to `inventory`.

Playbook: Refer to `site.yml`.

Run the playbook:

    ansible-playbook site.yml

You will need to reboot after running this playbook because macOS defaults are cached.

License
-------

BSD
