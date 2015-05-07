OSSEC
=========

[![Build Status](https://travis-ci.org/gotansible/ossec.svg)](https://travis-ci.org/gotansible/ossec)

Install OSSEC Server, Agent and/or Local

Requirements
------------

SSL Certificate and Key for the Server for auto registration. Use of the playbook gotansible.selfsign can help.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

* gotansible.selfsign - recommended for creating a self signed cert

Example Playbook
----------------

See test-agent.yml or test-server.yml.

    - hosts: servers
	  sudo: true
      roles:
         - { role: gotansible.ossec, ossec_server: true }

License
-------

MIT

Author Information
------------------

Created by Franklin Wise in Santa Monica, CA.
