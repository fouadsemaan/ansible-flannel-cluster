andrewrothstein.flannel-cluster
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

```ini
# inventory.ini
[flannel-master]
host[1:k].test

[flannel]
host[1:n].test

[etcd-master]
host[1:k].test
```

```yml
# playbook.yml
- hosts: flannel
  roles:
    - andrewrothstein.flannel-cluster 
```

License
-------

MIT

Author Information
------------------

* Fouad Semaan <semaanfouad@gmail.com>
* Andrew Rothstein <andrew.rothstein@gmail.com>
