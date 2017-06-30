Ansible Role: CentOS Repository
=========

An Ansible Role that to manage CentOS original Yum repository

Requirements
------------

This role needs no special requirements, except sudo access

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


```yaml
---
repo_location:              indonesia   # available options: international, indonesia, klog, vagrant
centos_base_enabled:        yes
centos_updates_enabled:     yes
centos_extras_enabled:      yes
centos_centosplus_enabled:  yes
centos_cr_enabled:          no
centos_fasttrack_enabled:   no
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
- name: Prepare CentOS 7 server
  hosts: centos7
  roles:
    - role: adipriyantobpn.repo-centos
      repo_location:              international
      centos_base_enabled:        yes
      centos_updates_enabled:     yes
      centos_extras_enabled:      yes
      centos_centosplus_enabled:  no
      centos_cr_enabled:          no
      centos_fasttrack_enabled:   no
```

License
-------

BSD

Author Information
------------------

This role was created in 2017 by [Adi Priyanto](https://github.com/adipriyantobpn) as a learning purpose for community.