# Ansible Rancher Role

A role to install and configure Rancher.

## Requirements

- Docker and Docker Compose

## Role Variables

- `rancher_version`: Specifies the version of Rancher (Optional)
- `rancher_http_port`: Specifies the HTTP port of Rancher (Optional)
- `rancher_https_port`: Specifies the HTTPS port of Rancher (Optional)
- `rancher_bootstrap_password`: Specifies the bootstrap password (Required)

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-rancher
      vars:
        rancher_version: "v2.11.1"
        rancher_bootstrap_password: "password"
```

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.
