# influx-grafana
Docker-Compose project to setup influxdb and grafana quickly.

---

Start service with `docker-compose up -d --build`.

Data is held under `/var/influxdb` and `/var/grafana` on host.

Login to grafana with `admin:admin`, then config datasource as `http://influxdb:8086`
