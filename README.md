ansible-role-pycharm
====================

Install [JetBrains PyCharm](https://www.jetbrains.com/pycharm).

Requirements
------------

None.

Role Variables
--------------

The default variables in `defaults/main.yml` are setup for an install in the \$HOME directory of the user running ansible.
Tweak as you like.

    pycharm_installation_location: "{{ ansible_env.HOME }}/pycharm"

Install into this final location.

    pycharm_download_location: "{{ ansible_env.TMPDIR }}"

Use this directory as temporary download/unpack location.

    pycharm_desktopicon_location: "{{ ansible_env.HOME }}/.local/share/applications"

Install generated .desktop entry into this location.

    pycharm_version: 2016.1.4
    pycharm_edition: professional

Pull and install this version and edition.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
         - { role: azmodude.pycharm }

License
-------

BSD

Author Information
------------------

None.
