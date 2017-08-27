Ansible Role: Webserver (Nginx)
=========

This role installs and configure a webserver. For the moment, this role only manages *Nginx*.

The following actions are performed:
- Install the latest version of Nginx
- Install the latest version of PHP-FPM
- Install the latest version of UFW
- Remove the default Website of Nginx
- Copy some hardened website templates to /root/
- Open the HTTP and HTTPS ports in the firewall
- Prepare the skeleton of new users to handle Websites

Requirements
------------

No specific requirements for this role.

Role Variables
--------------

No variables for this role.

Dependencies
------------

No dependencies from other roles required.

Example Playbook
----------------

Here is a simple example playbook to use this role:

```
hosts: web_srv
user: root
roles:
  - { role: webserver, tags: [ 'webserver' ] }
```

License
-------

MIT / BSD

Author Information
------------------

My name is Gaétan. You can follow me on [Twitter](https://twitter.com/gaetanict)

Website: [ICT Pour Tous](https://www.ictpourtous.com)
