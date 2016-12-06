MyCluster Ansible playbook
=========

Playbook Ansible pentru instalarea si configurarea infrastructurii aplicatiei RomanescI

Requirements
------------

Ansible installation URL: http://docs.ansible.com/ansible/intro_installation.html#

Will not work on Windows

Configuration
-------------

Rename hosts_sample to `hosts` and fill in the IPs for every machine. Roles are split into groups (pretty much self-explanatory):

* elasticsearch_nodes - Main Elasticsearch nodes
* webservers - Nginx webservers
* ha_proxy - Load balancer instance
* es_backup - Elasticsearch back-up repository

Example usage
----------------

Ideally, Ansible should be run from a host that has a private key with public keys installed on all hosts

1. Running with private keys installed on all hosts

    
> ansible-playbook  -b -i hosts -u ubuntu [playbook].yml
    
2. Running with prompt for SSH password and sudo password
    
    
> ansible-playbook -bkK -i hosts -u ubuntu [playbook].yml

> ansible-playbook -i hosts -ku root install.yml

3. Testing the playbook syntax

> ansible-playbook --syntax-check install.yml




License
-------

MIT

Author Information
------------------

**Made with :heart: by [GovITHub](http://ithub.gov.ro)**
