# prometheus-example

Example how to setup prometheus for monitoring and alerting.

node-exporter and cadvisor nodes are monitored as target nodes.

```
$ docker-compose up

### prometheus ui
$ open http://localhost:9090

### graphana (admin/admin)
$ open http://localhost:3000

### alertmanager ui
$ open http://localhost:9093
```
