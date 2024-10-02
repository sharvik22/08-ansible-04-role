clickhouse
=========

Install  clickhouse 

Role Variables
--------------

| vars                     | description                   |
|------------------------- |-------------------------------|
| {clickhouse_version}     | version clickhouse to install |
| {clickhouse_user}        |            netology           |
| {clickhouse_password}    |            netology           |
| {clickhouse_config_path} |   These are variables that point to the paths to the ClickHouse server configuration files | 
| {clickhouse_users_path } |  These are variables that point to the paths to the ClickHouse server configuration files  |




Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: clickhouse }

License
-------

MIT

Author Information
------------------
Viktor Sharapat