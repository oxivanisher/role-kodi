kodi
====

This role installs signal kodi.

Once upon a time, it used the PPA-Repo. But since it's no longer mainained, it now installs the flatpack on ubuntu.

Example Playbook
----------------
```yaml
- name: Install kodi
  hosts: client
  collections:
    - oxivanisher.kodi
  roles:
    - role: oxivanisher.linux_desktop.kodi
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_desktop](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_desktop/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_desktop).
