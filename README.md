Role Name
=========

Cassandra role to create a dockerized multi-node cassandra cluster.

Requirements
------------

Ensure that the target nodes have docker installed.

Role Variables
--------------

* `cluster_name`: Name of the cluster
* `num_tokens`: Number of tokens
* `data_file_directories`: Data file directories in array format

  Eg: [/var/lib/cassandra/data,/media/mydisk]


* `commitlog_directory`: Commitlog directory
* `saved_caches_directory`: Saved caches directory
* `endpoint_snitch`: Endpoint snitch (Eg: SimpleSnitch, GossipingPropertyFileSnitch)
* `rack`: Name of the rack
* `dc`: Name of the DC


Dependencies
------------

Either install Docker as mentioned requirements or install some ansible role which installs docker.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: cassandra_servers
      roles:
         - { role: bingoarun.cassandra-docker-cluster }

License
-------

GNU

Author Information
------------------

Arun prasath
