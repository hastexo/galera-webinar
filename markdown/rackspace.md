<!-- .slide: data-background-image="images/rackspace-logo.svg" data-background-size="contain" -->
### Rackspace Private Cloud <!-- .element class="fragment" -->
Note: RPC v10 is based on Juno; RPC v11 on Kilo. Most documentation on
docs.rackspace.com is currently available for v10; the v11
documentation is only available from GitHub at
https://github.com/stackforge/os-ansible-deployment/.


Default deployment stack
## Ansible
Note: Reference: http://docs.rackspace.com/rpc/api/v10/bk-rpc-installation/content/index.html

It's important to understand that RPC is geared towards Ubuntu only;
more specifically Ubuntu Trusty (see
http://docs.rackspace.com/rpc/api/v10/bk-rpc-installation/content/sec-hosts-deployment-os.html).


### Foundation playbook
### `setup-hosts.yml`


### Infrastructure playbook
### `setup-infrastructure.yml`
Note: This installs
- Memcached
- Galera
- RabbitMQ
- rsyslog
- ELK (ElasticSearch, Logstash, Kibana)


### OpenStack playbook
### `setup-openstack.yml`
