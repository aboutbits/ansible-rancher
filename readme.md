# Ansible Rancher Role

A role to install and configure Rancher.

## Requirements

- Docker and Docker Compose

## Role Variables

- `rancher_version`: Specifies the version of Rancher (Optional)
- `rancher_admin_password`: Specifies the password of the admin user (Required)
- `rancher_http_port`: Specifies the HTTP port of Rancher (Optional)
- `rancher_https_port`: Specifies the HTTPS port of Rancher (Optional)
- `rancher_url`: Specifies the URL of Rancher under which it is reachable (Required)

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-rancher
      vars:
        rancher_version: "v2.11.1"
        rancher_admin_password: "password"
        rancher_url: "https://rancher.example.com"
```

## Versioning

In order to have a versioning in place and working, create lightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag v1
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d v1
git push origin :refs/tags/v1
git tag v1
git push --tags
```
