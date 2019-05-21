ansible-certbot-role
=========

Certbot supported certificate management for Debian.

Note: Debian supports automatic renewal via cron, systemd.

Requirements
------------

None

Role Variables
--------------
```YAML
##
# Defaults for certbot support
##

# Enable certbot support
certbot_enabled: true

# Create missing certificates
certbot_create_missing: true

#
# Nginx support will add certificates automatically to the nginx vhost. 
# Caution: Existing vhost config will be changed!
# 
# Standalone will only create certificates, but you need to manually add 
# them to your webserver configuration.
#
certbot_plugin: standalone # nginx|standalone

##
# Certbot certificate setup example
##
certbot_certificates:
  - email: email@example.tld
    domain: example.tld
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: methorz.certbot}

License
-------

BSD

Author Information
------------------

https://twitter.com/methor_z
