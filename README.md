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

* `openvpn_client_server`: FQDN of the VPN server
Mandatory

* `openvpn_client_server_home`: Should be equal to the setting of `openvpn_server_home` in the ansible-openvpn-server configuration
Default: "/etc/openvpn"

* `openvpn_client_proto`: Protocol of the VPN server
Default: "udp"

* `openvpn_client_port`: Port on the VPN server
Default: 1194

* `openvpn_client_dev`: Device to use for the VPN
Default: "tap"

* `openvpn_client_dev_type`: Device type to use (tun or tap)
Default: "tap"

* `openvpn_client_home`: Home of the OpenVPN daemon
Default: /etc/openvpn

* `openvpn_client_user`: User to run OpenVPN as
Default: openvpn

* `openvpn_client_group`: Group to run OpenVPN as
Default: openvpn

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
