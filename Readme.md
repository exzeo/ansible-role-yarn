Ansible Role Yarn
=========

Installs Helm Command Line on Debian/Ubuntu servers. 
Releases: https://github.com/yarnpkg/yarn/releases

Role Variables
--------------

```
# Version of 'yarn' to install, defaults to latest version
yarn_version: ""

# Toggling this will uninstall from the server
uninstall: false
```


Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.yarn
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.yarn
      vars:
        yarn_version: "1.22.0-1"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.yarn
      vars:
        uninstall: true
```