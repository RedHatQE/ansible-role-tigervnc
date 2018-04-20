Role Name
=========

This plugin helps with installing and configuring of `TigerVNC` server.
Actually it can install the package on a linux with an old way to start/configure system service (ie. not using systemd)

Requirements
------------

Role Variables
--------------

see ./defaults/main.yml

- VNC_SERVER_ARGS - arguments that vncserver starts with
- VNC_DISPLAY: - a number of a vnc display
- VNC_USER: user you log in with
- VNC_PASSWORD: a password for the user


Dependencies
------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: tigervnc-server, VNC_SERVER_ARGS: "-geometry 800x600", 
                                    VNC_DISPLAY:2, 
                                    VNC_USER: root,
                                    VNC_PASSWORD: password }

Do not forget to open firewall port once you want to connect the system remotely.

The right port is: `5900 + VNC_DISPLAY`

License
-------

BSD

Author Information
------------------

TODO
- [ ] systemd based system included
