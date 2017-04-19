FROM ubuntu:14.04

RUN apt-get update
RUN apt-get install -y wget

RUN wget https://dl.influxdata.com/influxdb/releases/influxdb_1.2.2_amd64.deb
RUN dpkg -i influxdb_1.2.2_amd64.deb

#ADD influx.conf /etc/influx.conf

RUN influxd config > /etc/influx.conf

EXPOSE 8083

EXPOSE 8086

CMD ["/usr/bin/influxd", "-config", "/etc/influx.conf"]
