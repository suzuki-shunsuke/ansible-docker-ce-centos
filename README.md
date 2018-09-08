# ansible-docker-ce-centos

[![GitHub last commit](https://img.shields.io/github/last-commit/suzuki-shunsuke/ansible-docker-ce-centos.svg)](https://github.com/suzuki-shunsuke/ansible-docker-ce-centos)
[![GitHub tag](https://img.shields.io/github/tag/suzuki-shunsuke/ansible-docker-ce-centos.svg)](https://github.com/suzuki-shunsuke/ansible-docker-ce-centos/releases)
[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/suzuki-shunsuke/ansible-docker-ce-centos/master/LICENSE)

ansible role to install Docker CE on CentOS

https://galaxy.ansible.com/suzuki-shunsuke/docker-ce-centos/

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_version | no | latest | | docker version
docker_centos_state | no | undefined (do nothing) | "started" or "stopped" or "restarted" or "reloaded" | docker daemon state
docker_centos_enabled | no | undefined(do nothing) | | whether docker daemon is enabled
docker_centos_users | no | [] | ["vagrant"] | users added to docker group

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.docker-ce-centos
    docker_centos_state: started
    docker_centos_enabled: yes
    docker_centos_users:
    - vagrant
    become: yes
```

## License

[MIT](LICENSE)
