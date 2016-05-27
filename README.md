Ansible php-fpm role.
=========
[![Build Status](https://travis-ci.org/spitfast/ansible-php-fpm-role.svg?branch=master)](https://travis-ci.org/spitfast/ansible-php-fpm-role)

An ansible role for php-fpm installation.

Requirements
------------

Ansible version **2.0.1** or higher.

Role Variables
--------------

```yaml
php_fpm_package: php7.0-fpm
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
---
- hosts: servers
  roles:
   - spitfast.php-fpm
```

License
-------

MIT

Author Information
------------------

[Gordon Shumway](https://github.com/spitfast/)
