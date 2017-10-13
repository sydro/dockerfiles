# Ansible docker container

Ansible is a radically simple IT automation system. It handles configuration-management, application deployment, 
cloud provisioning, ad-hoc task-execution, and multinode orchestration - including trivializing things like 
zero downtime rolling updates with load balancers.

Read the documentation and more at https://ansible.com/

This is an Ubuntu 16.04 container with installation of ansible via pip.


## Starting a container

```
docker run sydro/ansible ansible view --help
```
