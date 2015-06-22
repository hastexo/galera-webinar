<!-- .slide: data-background-image="images/ubuntu-logo.svg" data-background-size="contain" -->
### Ubuntu OpenStack <!-- .element class="fragment" -->


Default deployment stack
## Landscape
## MAAS
## Juju
Note: Reference: http://www.ubuntu.com/download/cloud/install-ubuntu-openstack


Deployment checklist
# 1
### Install MAAS server


```sh
add-apt-repository ppa:maas-maintainers/stable
add-apt-repository ppa:cloud-installer/stable
add-apt-repository ppa:juju/stable
apt update
apt install maas
```


Deployment checklist
# 2
### Wire MAAS up with Landscape


```sh
apt install openstack
openstack-install
```
Choose `Landscape OpenStack Autopilot`


Deployment checklist
# 3
### Install OpenStack from Landscape


<!-- .slide: data-background-image="http://assets.ubuntu.com/sites/ubuntu/1410/u/img/download/cloud/install-ubuntu-cloud-step4.png" data-background-size="contain" -->


### Don't like Landscape?


Ubuntu OpenStack
## Multi Installer


```sh
apt install openstack
openstack-install
```
Choose `Multi-system`
Note: This still requires MAAS. The `Single system` option does not, but it also assumes that **everything** runs on the same node (in LXC containers).

References:
- http://ubuntu-cloud-installer.readthedocs.org/en/latest/single-installer.guide.html
- http://ubuntu-cloud-installer.readthedocs.org/en/latest/multi-installer.guide.html


### Don't like MAAS?


### Juju `manual` environment


```sh
juju bootstrap
juju deploy [...]
```
