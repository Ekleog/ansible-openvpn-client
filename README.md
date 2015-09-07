openvpn-client
==============

This role aims to provide an easy-to-use (yet flexible) OpenVPN client configuration.

It is designed to work together with openvpn-server ; this way it can efficiently create required groups and
fetch configuration files directly from the servers. No configuration duplication is required: all the configuration
is generated on the server, this role is just used as a helper to more easily deploy configuration.

Requirements
------------

At the moment, only portage is supported. Adding support for other package managers should be trivial, though.

Role Variables
--------------

* `openvpn_client_home`: Directory in which to place configuration files
Default: /etc/openvpn

Tags
----

* `openvpn-client-pkgs`: Installs required packages

* `openvpn-client-user`: Add asked user and group if needed

* `openvpn-client-config`: Fetches OpenVPN configuration files

Example Playbook
----------------

TODO

License
-------

GPLv3

Author Information
------------------

If needed, you can contact me at <leo@gaspard.io>.
