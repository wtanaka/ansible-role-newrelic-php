[![Build Status](https://travis-ci.org/wtanaka/ansible-role-newrelic-php.svg?branch=master)](https://travis-ci.org/wtanaka/ansible-role-newrelic-php)
[![CircleCI](https://circleci.com/gh/wtanaka/ansible-role-newrelic-php.svg?style=svg)](https://circleci.com/gh/wtanaka/ansible-role-newrelic-php)

wtanaka.newrelic-php
====================

Ansible role to install newrelic-php agent.

This playbook runs newrelic-install after installing the debian
package.  If this fails to identify your PHP installation, you may
have to follow the non-standard PHP instructions in
https://docs.newrelic.com/docs/agents/php-agent/advanced-installation
instead.

NOTE: You must restart your PHP runtime (fpm, or apache) after this
role runs.

Example Playbook
----------------

    - hosts: all
      roles:
         - role: wtanaka.newrelic-php
           newrelic_php_application_name: my app name
           newrelic_php_license_key: LICENSE_KEY_HERE

Or you can include just the role, and configure it in `host_vars`

    PLAYBOOK
    - hosts: all
      roles:
         - wtanaka.newrelic-php

    HOST_VARS file:
    newrelic_php_application_name: my app name
    newrelic_php_license_key: LICENSE_KEY_HERE

If your PHP binary is not in the PATH, this role will probably not
work, because newrelic-install assumes that it is.

However, you can set:

`newrelic_php_binary: /path/to/your/php`

and if newrelic is already installed, this role is designed to skip
the newrelic-install run

License
-------

GPLv2

Author Information
------------------

http://wtanaka.com/
