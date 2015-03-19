rbenv
=========

[![Join the chat at https://gitter.im/joiggama/ansible-rbenv](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/joiggama/ansible-rbenv?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This ansible role aims to install [rbenv](https://github.com/sstephenson/rbenv) on ubuntu systems.

Requirements
------------

The only dependency is `git` and it's already included in the main tasks, if you don't want this role to install it, override the default variable `install_dependencies` to equal `false` when including this role.

Role Variables
--------------

| Name                 | Default                           |                                        |
|:--------------------:|:---------------------------------:|:--------------------------------------:|
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
       install_dependencies: true
       root:                 ~/.rbenv
       version:              v0.4.0
```


License
-------

The [MIT license](LICENSE.md)
