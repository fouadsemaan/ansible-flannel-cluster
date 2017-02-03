andrewrothstein.flannel-cluster
===========================

* Configures a TLS secured flannel cluster
* Installs flannel on each host in the ```flannel``` group
* Runs a flanneld server on each host in the ```flannel-master``` group
* Finds the etcd cluster through the ```etcd-master``` group 

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
    - role: andrewrothstein.flannel-cluster 
```

License
-------

MIT

Author Information
------------------

* Fouad Semaan <semaanfouad@gmail.com>
* Andrew Rothstein <andrew.rothstein@gmail.com>
