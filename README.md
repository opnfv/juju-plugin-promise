Promise Juju charm
============

Promise plugin
-----------------------

Overview
--------

This will install Promise onto virtual machines for Resource Management via Juju

* [OPNFV Promise](https://wiki.opnfv.org/promise) Resource Management

Requirements
------------

| Requirement                      | Version/Comment   |
|----------------------------------|-------------------|
| Juju test Environment            | 1.24.7 and above  |

Recommendations
---------------

LXC as hypervisor to test.

Installation Guide
==================

Promise plugin installation
----------------------------------------

1. Prepare work directory on Juju test host:

        mkdir -p ~/charms/trusty
        
2. Clone the juju-plugin-promise repo from github:

        git clone  https://github.com/opnfv/juju-plugin-promise.git opnfv-promise

3. Prepare Juju local environment:

        juju bootstrap

4. Deploy juju charm server:

        juju deploy --repository=/<path to work dirctory>/charms local:trusty/opnfv-promise

5. Check the installation progress

        juju -v status

6. Check if the plugin was installed successfully:

        Check log under ~/.juju/local/log/

        2016-01-12 06:26:16 INFO start Starting promise...                               Ok

## License
  [Apache-2.0](LICENSE)
