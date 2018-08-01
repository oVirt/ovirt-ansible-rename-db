oVirt Engine dump
=================

This role changes name of oVirt engine and DWH database.

- rename databases (engine or DWH)
- set new names in engine config files

Target systems
--------------

* engine

Requirements
------------

Preinstalled engine with local DB.

Role Variables
--------------

```yaml
---
ovirt_engine_db_name: new name of the engine database
ovirt_engine_db_name_dwh: new name of the dwh database
ovirt_engine_version: oVirt engine X.Y version (default: 4.2)
```

Dependencies
------------

Role ansible-role-ovirt-dump-db

Example Playbook
----------------

```yaml
---
- hosts: engine
  vars:
    ovirt_engine_db_name: "my_engine"
  roles:
    - ansible-role-ovirt-rename-db
```

Author Information
------------------

Lucie Leistnerova
lucie.leistnerova@gmail.com
