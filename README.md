fouadsemaan.flannel-cluster
===========================

Configures a flannel cluster. 
Runs a flannel daemon on each host in group flannel-group against an existing etcd-cluster.

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

inventory.ini
```ini
[flannel-group]
host[1:n].test

[etcd-master]
host[1:m].test
```

in your playbook:
```yml
- hosts: flannel-group 
  roles:
    - fouadsemaan.flannel-cluster 
```

License
-------

MIT

Author Information
------------------

Fouad Semaan semaanfouad@gmail.com
