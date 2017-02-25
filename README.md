gchiesa.glusterfs
=================

Role that installs glusterfs cluster

Requirements
------------


Role Variables
--------------

an extra module can be activated in order to setup the cluster in order to be used by docker swarm 

```
extra_modules = ["docker"]
```

The complete list of variables is the following:
```
# iptables configuration file
iptables_config: "/etc/sysconfig/iptables"

extra_modules: []
# use root to force gluster on the root partition
gluster_force_root_partition: true
gluster_volumes:
    - /glusterfs/brik1/gv0
```

Dependencies
------------

none 

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: 'gchiesa.glusterfs', extra_modules: ['docker'] }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
