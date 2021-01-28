Ansible role for docker
==================================

Installs Docker

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-docker/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-docker/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-docker/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-docker/actions?query=workflow%3A%22Release%22)

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
|`docker_architecture`|Architecture of Docker to install|string|`x86_64`|false|
|`docker_distro`|Distro of Docker to install|string|`linux`|false|
|`docker_download_url`|URL of Docker binary|string|`https://download.docker.com/{{ docker_distro }}/static/stable/{{ docker_architecture }}/docker-{{ docker_version }}.tgz`|false|
|`docker_state_directory`|Directory of Docker state|string|`/var/lib/docker`|false|
|`docker_user`|User to add to the `docker` group|string|`docker`|false|
|`docker_version`|Version of Docker to install|string|`20.10.2`|false|

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ansible-role-docker
      vars:
        docker_user: ubuntu
```

License
-------

[Apache License](LICENSE)
