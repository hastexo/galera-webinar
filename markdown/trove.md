What about
# Trove?


Trove:
## Database as a service
in OpenStack


Think
# RDS
## + DynamoDB
in AWS


Trove makes
## Database deployment
in OpenStack easy


```
trove create <dbname> <flavor> \
  --datastore mysql \
  --datastore_version 5.5
```
(creates database) <!-- .element class="fragment" -->


```
trove create <dbname> <flavor> \
  --replica_of <source_instance> \
  --replica_count 5
```
(configures MySQL master/slave replication) <!-- .element class="fragment" -->


# But:
No Galera cluster support yet

(only MongoDB clustering) <!-- .element class="fragment" -->