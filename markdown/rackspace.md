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


Deployment checklist
# 1
### Install deployment host


```sh
cd /opt
git clone https://github.com/stackforge/os-ansible-deployment.git
pip install -r /opt/os-ansible-deployment/requirements.txt
```


Deployment checklist
# 2
### Configure target hosts
Note: This effectively comprises editing a bunch of YAML configuration
files for Ansible to describe your target host topology.


Deployment checklist
# 3
### Run Ansible playbooks


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
