lighthouse
=========

Install lighthouse
Install Git

Requirements
------------

Install Git
Install Nginx

Role Variables
--------------

| vars                          | description                   |
|------------------------------ |-------------------------------|
| {clickhouse_user}             |            netology           |
| {clickhouse_password}         |            netology           |
| {lighthouse_dir}              |    Lighthouse data and configuration files | 
| {lighthouse_access_log_name } |    the name of the file to which Lighthouse access logs will be written |
| {lighthouse_vcs}              | (https://github.com/VKCOM/lighthouse.git) |


Dependencies
------------

clickhouse-role

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: vector
      roles:
      - { role: lighthouse-role }

License
-------

MIT

Author Information
------------------
Viktor Sharapat