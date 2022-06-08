```
docker run --name loki -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:2.4.2 -config.file=/mnt/config/loki-config.yaml
docker run -v $(pwd):/mnt/config -v /var/log:/var/log --link loki grafana/promtail:2.4.2 -config.file=/mnt/config/promtail-config.yaml
```
