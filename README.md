Role Name
=========

Base configuration for a new Ubuntu GNU/Linux box.

Requirements
------------

This role is only maintained for Ubuntu GNU/Linux 18.04 and above.

Role Variables
--------------


| Parameters     | Default Value | Comments                                    |
|----------------|---------------|---------------------------------------------|
| admin_users    | []            | An array of users with sudo permissions.    |
| standard_users | []            | An array of users without sudo permission.  |
| other_packages | []            | An array of packages to install by default. |

Dependencies
------------

This role does not rely on any third-party roles.

Example Playbook
----------------

```yaml
- name: Base configuration
  base_role:
    admin_users:
      - john
      - george
    standard_user:
      - paul
      - ringo
    other_packages:
      - emacs
      - htop
      - cowsay
```

License
-------

CC-BY-4.0

Author Information
------------------

https://plume.baucum.me
