# docker-monitoring

## Docker-compose install

```bash
# skip this if you already have docker installed 
apt install docker.io -y
# on ubuntu os
curl -SL https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## Boot

```bash
docker-compose up -d
```

Ensure all containers are running:

```bash
docker-compose ps
```

## Endpoints

The following endpoints are available:

| Container      | Internal Endpoint         | External Endpoint     |
| -------------- | ------------------------- |---------------------- |
| Grafana        | <http://grafana:3000>       | <http://localhost:3000> |
| Prometheus     | <http://prometheus:9090>    | <http://localhost:9090> |
| Node-Exporter  | <http://node-exporter:9100> | <http://localhost:9100> |
| cAdvisor       | <http://cadvisor:8080>      | N/A                   |

## Cleanup

```bash
docker-compose down
```
