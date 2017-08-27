Monitoring-Stack(s)
===================

- Prometheus is the first to be implemented like this The `prometheus-server/docker-compose.yml` will provide a docker-compose '3.2' api version compatibility for docker swarm.
- TODO -> add a docker-compose-2.yml for backward/single node deployments

Naming convention
=================

`*-exporter` - stands for the exporter - unless it's self explanitory a README.md will be present for each.
The `prometheus-server` is SWARM ready and might make some of these redundednt (not to mantion code duplication ...)
