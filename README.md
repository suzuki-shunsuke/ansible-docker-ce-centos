# ansible-docker-ce-centos

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
