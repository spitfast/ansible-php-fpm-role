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
php_branch_version: 7.0
php_fpm_package: php{{ php_branch_version }}-fpm
php_fpm_extensions: # List of extensions without php version prefix.
  - cli
  - common
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
---
- hosts: localhost
  roles:
   - spitfast.php-fpm
```
Or you can pass variables to playbook to override default vars. For example, for php 5.6
```yaml
---
- hosts: all
  roles:
    - {
        role: spitfast.php-fpm,
        php_branch_version: 5.6
      }
```
Usage
----
Create playbook (described in the section above) and run one of the following commands:

`$ ansible-playbook playbook.yml` - to run all tasks in role

`$ ansible-playbook playbook.yml --tags=php-extensions` - to install php extensions listed in **{{php_fpm_extensions}}** variable (see **Role Variables** section)

License
-------

MIT

Author Information
------------------

[Gordon Shumway](https://github.com/spitfast/)
