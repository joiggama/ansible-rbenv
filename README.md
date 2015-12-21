rbenv
=========

[![travis](https://img.shields.io/travis/joiggama/ansible-rbenv/master.svg)](https://travis-ci.org/joiggama/ansible-rbenv)
[![gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/joiggama/ansible-ruby)

This ansible role aims to install [rbenv](https://github.com/sstephenson/rbenv) on ubuntu systems.

Requirements
------------

None.

Role Variables
--------------

| Name                       | Default                             |                                        |
|:--------------------------:|:-----------------------------------:|:--------------------------------------:|
| rbenv_apt_cache_expiration | 3600                                | Update apt cache window in seconds     |
| rbenv_install_dependencies | true                                | Whether or not to install dependencies |
| rbenv_root                 | /home/{{ ansible_env.USER }}/.rbenv | Install path for rbenv                 |
| rbenv_version              | master                              | Any git reference: branch, tag, commit |


Dependencies
------------

None.

Example Playbook
----------------

```yml
- gather_facts: true
  hosts:        all
  roles:
                - joiggama.rbenv
```


License
-------

[MIT](LICENSE.md)
