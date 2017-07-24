# ansible-docker-ce-centos

ansible role to install Docker CE on CentOS

https://galaxy.ansible.com/suzuki-shunsuke/docker-ce-centos/

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_version | no | latest | | docker version
docker_centos_started | no | do nothing | | whether docker daemon is started
docker_centos_enabled | no | do nothing | | whether docker daemon is enabled
docker_centos_users | no | [] | ["vagrant"] | users added to docker group

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.docker-ce-centos
    docker_centos_started: yes
    docker_centos_enabled: yes
    docker_centos_users:
    - vagrant
    become: yes
```

## License

[MIT](LICENSE)
