# ansible-docker-ce-centos

ansible role to install Docker CE on CentOS

https://galaxy.ansible.com/suzuki-shunsuke/docker-ce-centos/

Requirements
------------

Nothing.

Role Variables
--------------

* docker_centos_version: docker version. The default is latest.
* docker_centos_started: whether docker daemon is started. The default is "no".
* docker_centos_enabled: whether docker daemon is enabled. The default is "no".
* docker_centos_users: users added to docker group. The default is "[]".

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.docker-ce-centos
    docker_centos_version: 17.03.1.ce-1.el7.centos
    docker_centos_started: yes
    docker_centos_enabled: yes
    docker_centos_users:
    - vagrant
```

License
-------

MIT
