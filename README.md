ASBRL-POSTGRESQL-EXPORTER
=========

Deploy a PostgreSQL-Exporter as a Docker container.

Requirements
------------

- Need to be Docker engine installed.
- A PostgreSQL running to get Metrics from there.

Role Variables
--------------

- default_user: 'ubuntu'
- BUILD: ''
- PG_HOST: 'localhost'
- PG_PORT: 5432
- PG_USERNAME: ''
- PG_PASSWORD: ''
- CONTAINER_NAME: "postgres-exporter"
- DOCKER_CPU_PERIOD: 0
- DOCKER_CPU_QUOTA: 0
- DOCKER_MEMORY: 0
- CONTAINER_STATE: 'started'

Dependencies
------------

None

Example Playbook
----------------


    - name: Deploy PostgreSQL Exporter
      include_role:
        name: asbrl-postgresql-exporter
      vars:
        PG_USERNAME: "{{ PG_ROOT_USERNAME }}"
        PG_PASSWORD: "{{ PG_ROOT_PASSWORD }}"
      tags:
        - asbrl-postgresql-exporter

License
-------

BSD

Author Information
------------------

Moegui.com
