Vector
=========

Install Vector

Role Variables
--------------

| vars| description|
|--------------------------------- |-------------------------------|
| {clickhouse_user}                |            netology           |
| {clickhouse_password}            |            netology           |
| { ansible_architecture}          |     system architecture       | 
| { ansible_user_id }              |              UID              |
| { ansible_user_gid }             |              GID              |
| { vector_config_path }           | to the path to the Vector configuration file |
| { vector_config | to_nice_yaml } |  This variable contains the Vector configuration converted into human-readable YAML format |

Dependencies
------------

clickhouse-role

Example Playbook
----------------

    - hosts: vector
      roles:
      - { role: vector-role }

License
-------

MIT

Author Information
------------------
Viktor Sharapat