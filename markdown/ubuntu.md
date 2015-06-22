<!-- .slide: data-background-image="images/ubuntu-logo.svg" data-background-size="contain" -->
### Ubuntu OpenStack <!-- .element class="fragment" -->


Default deployment stack
## Landscape
## MAAS
## Juju
Note: Reference: http://www.ubuntu.com/download/cloud/install-ubuntu-openstack


<!-- .slide: data-background-image="http://assets.ubuntu.com/sites/ubuntu/1410/u/img/download/cloud/install-ubuntu-cloud-step4.png" data-background-size="contain" -->


```
mysql:
  vip: '192.168.77.8'
  root-password: agoodpassword
  sst-password: agoodpassword
mysql-hacluster:
  corosync_transport: unicast
```


```
juju deploy --config local.yaml -n 3 percona-cluster mysql
juju deploy --config local.yaml hacluster mysql-hacluster
juju add-relation mysql mysql-hacluster
```