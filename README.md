# prometheus-example

Example how to setup prometheus for monitoring and alerting.

node-exporter, cadvisor and aspnetapp are monitored as target nodes.

```
$ docker-compose up

### prometheus ui
$ open http://localhost:9090

### graphana (admin/admin)
$ open http://localhost:3000

### alertmanager ui
$ open http://localhost:9093

### aspnetapp
$ curl http://localhost:12345/api/values // will increase 'myCounter' counter
$ curl http://localhost:12345/metrics
```

To stress test aspnetapp use vegeta:

```
$ docker run oba11/vegeta sh -c 'echo "GET http://localhost:12345/api/values" | vegeta attack -duration=10s | tee results.bin | vegeta report'
```
