kodi
====

This role installs the kodi mediacenter.

Once upon a time, it used the PPA-Repo. But since it is no longer mainained, it now installs the flatpack on ubuntu.

If the variables are set, this role also copies background images for kodi with a script that changes it and it is able to configure `advancedsettings.xml` to use kodi with a centralized MySQL.

Role Variables
--------------

| Name                    | Comment                               | Default value |
|-------------------------|---------------------------------------|---------------|
| kodi_os_user            | The OS user for which `advancedsettings.xml` and the background images are configured |  |
| kodi_mysql_host         | The MySQL host                        | |
| kodi_mysql_port         | The MySQL port                        | |
| kodi_mysql_username     | The MySQL user                        | |
| kodi_mysql_database     | The MySQL database                    | |
| kodi_mysql_password     | The MySQL password                    | |
| kodi_metadata_share     | A smb or nfs share where the metadata will be stored centralized | |
| kodi_webserver_username | The webserver username to be set      | |
| kodi_webserver_password | The webserver password to be set      | |
| kodi_wins_server        | The WINS server to be set             | |
| kodi_smb_workgroup      | The SMB workgroup to be set           | |
| kodi_sources            | A list of sources to be added to kodi | `[]` |


The `kodi_sources` variable is a list of sources in the form of `name`: `source`:

```yaml
kodi_sources:
  Source A: "nfs://server_a.domain.tld/path"
  Source B: "nfs://server_b.domain.tld/path"
```

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
