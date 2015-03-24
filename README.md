rbenv
=========

[![travis](https://img.shields.io/travis/joiggama/ansible-rbenv/master.svg)](https://travis-ci.org/joiggama/ansible-rbenv)
[![gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/joiggama/ansible-rbenv)

This ansible role aims to install [rbenv](https://github.com/sstephenson/rbenv) on ubuntu systems.

Requirements
------------

The only dependency is `git` and it's already included in the main tasks, if you don't want this role to install it, override the default variable `install_dependencies` to equal `false` when including this role.

Role Variables
--------------

| Name                 | Default                           |                                        |
|:--------------------:|:---------------------------------:|:--------------------------------------:|
| apt_cache_expiration | 3600                              | Update apt cache window in seconds     |
| install_dependencies | true                              | Whether or not to install dependencies |
| root                 | /home/{{ansible_env.USER}}/.rbenv | Install path for rbenv                 |
| version              | v0.4.0                            | Any git reference: branch, tag, commit |


Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: all
  roles:
     - role:                 joiggama.rbenv
       apt_cache_expiration: 3600
       install_dependencies: true
       root:                 ~/.rbenv
       version:              v0.4.0
```


License
-------

The [MIT license](LICENSE.md)
