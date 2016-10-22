[![Build Status](https://travis-ci.org/wtanaka/ansible-role-newrelic-php.svg?branch=master)](https://travis-ci.org/wtanaka/ansible-role-newrelic-php)
[![CircleCI](https://circleci.com/gh/wtanaka/ansible-role-newrelic-php.svg?style=svg)](https://circleci.com/gh/wtanaka/ansible-role-newrelic-php)

wtanaka.newrelic-php
====================

Ansible role to install newrelic-php agent

Example Playbook
----------------

    - hosts: all
      roles:
         - role: wtanaka.newrelic-php
           newrelic_php_application_name: my app name
           newrelic_php_license_key: LICENSE_KEY_HERE

Or you can include just the role, and configure it in host_vars

    PLAYBOOK
    - hosts: all
      roles:
         - wtanaka.newrelic-php

    HOST_VARS file:
    newrelic_php_application_name: my app name
    newrelic_php_license_key: LICENSE_KEY_HERE

License
-------

GPLv2

Author Information
------------------

http://wtanaka.com/
