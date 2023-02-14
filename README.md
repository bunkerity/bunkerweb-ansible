BunkerWeb
=========

Ansible role to install and manage [BunkerWeb](https://docs.bunkerweb.io) on Linux.

See the [documentation](https://docs.bunkerweb.io/1.4/integrations/#ansible) for more information about the role.

Requirements
------------

We assume that you are already familiar with both BunkerWeb and Ansible.

Role Variables
--------------

| Name  | Type  | Description  | Default value  |
|:-----:|:-----:|--------------|----------------|
| `bunkerweb_version` | string | Version of BunkerWeb to install. | `1.4.5` |
| `nginx_version` | string | Version of NGINX to install. | `1.20.2` |
| `freeze_versions` | boolean | Prevent upgrade of BunkerWeb and NGINX when performing packages upgrades. | `true` |
| `variables_env` | string | Path of the variables.env file to configure BunkerWeb. | `files/variables.env` |
| `enable_ui` | boolean | Activate the web UI. | `false` |
| `custom_ui` | string | Path of the ui.env file to configure the web UI. | `files/ui.env` |
| `custom_configs_path` | Dictionary | Each entry is a path of the folder containing custom configurations. Keys are the type of custom configs : `http`, `server-http`, `modsec`, `modsec-crs` and `default-server-http` | empty values |
| `custom_www` | string | Path of the www directory to upload. | empty value |
| `custom_plugins` | string | Path of the plugins directory to upload. | empty value |
| `custom_www_owner` | string | Default owner for www files and folders. | `nginx` |
| `custom_www_group` | string | Default group for www files and folders. | `nginx` |

License
-------

AGPL v3
