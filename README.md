Role Name
=========

Base configuration for a new Ubuntu GNU/Linux box.

Requirements
------------

This role is only maintained for Ubuntu GNU/Linux 18.04 and above.

Role Variables
--------------

| Parameters        | Default Value | Comments                                                                                             |
|-------------------|---------------|------------------------------------------------------------------------------------------------------|
| admin_users       | []            | An array of users with sudo permissions.                                                             |
| allowed_ssh_users | []            | A list of additional users not listed in admin_users or standard_users that are also allowed to ssh. |
| standard_users    | []            | An array of users without sudo permission.                                                           |
| other_packages    | []            | An array of packages to install by default.                                                          |
| hostname          |               | The hostname of the machine                                                                          |

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
    hostname: ramesses
```

License
-------

CC-BY-4.0

Author Information
------------------

https://plume.baucum.me
