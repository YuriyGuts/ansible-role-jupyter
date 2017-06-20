yuriyguts.jupyter
=================

An Ansible role to install and configure [Jupyter](http://jupyter.org/) on Linux.
Optionally, it can install Jupyter server as a `systemd` daemon.


Role Variables
--------------

See [defaults/main.yml](defaults/main.yml).

_Note_: if the target environment requires running `pip` with elevated privileges,
make sure to set `jupyter_package_manager_become: yes` in your playbook.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: modeling
      roles:
        - role: yuriyguts.jupyter
          jupyter_ip: '*'
          jupyter_port: 8888
          jupyter_plaintext_password: jupytersecret
          jupyter_daemon_enable: yes

License
-------

MIT

Author Information
------------------

Yuriy Guts ([https://github.com/YuriyGuts](https://github.com/YuriyGuts)).
