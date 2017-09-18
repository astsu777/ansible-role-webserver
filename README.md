Ansible Role: Webserver (Nginx OR Apache)
=========

This role installs and configure a webserver. For the moment, this role only manages *Nginx* OR *Apache* (you can choose which one to install using a variable).

The following actions are performed:
- Install the latest version of Nginx or Apache
- Install the latest version of PHP-FPM
- Install the latest version of UFW
- Remove the default Website of the Web server
- Copy some hardened website templates to /root/
- Open the HTTP and HTTPS ports in the firewall
- Prepare the skeleton of new users to handle Websites

Requirements
------------

No specific requirements for this role.


Role Variables
--------------

By default, this role will install and configure Nginx. However, a variable can be set to choose Apache if you want to.

Here is the variable as defined by default in this role:

'''
webserver: nginx
'''

If you prefer to install Apache instead of Nginx, set the value of this variable to *apache*.


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
