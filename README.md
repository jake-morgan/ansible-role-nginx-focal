NGINX Focal Fossa
=========

![master](https://github.com/jake-morgan/ansible-role-nginx-focal/workflows/master/badge.svg)

Install NGINX on Ubuntu 20.04 LTS (Focal Fossa).

Simple role that installs and configures NGINX without many of the advanced options and features offered by other Galaxy roles.

Requirements
------------

Tested only on Ubuntu 20.04 LTS Focal Fossa. No guarantee it will work on other distros or Ubuntu versions.

Role Variables
--------------

| Variable | Description | Type| Required | Default |
|-|-|-|-|-|
| `uninstall_existing_nginx` | Remove existing NGINX installations. | Bool | No | `default` |
| `ufw_access` | Access Nginx has for UFW. Can be one of `Full`, `HTTP`, `HTTPS`, or, `none`. | String | No | `none` |

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: jake-morgan.nginx-focal
      vars:
        uninstall_existing_nginx: false
        ufw_access: Full
```

License
-------

MIT
