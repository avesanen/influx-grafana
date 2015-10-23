FROM ubuntu:14.04

RUN apt-get update
RUN apt-get install -y wget

RUN wget https://s3.amazonaws.com/influxdb/influxdb_0.9.4.1_amd64.deb
RUN dpkg -i influxdb_0.9.4.1_amd64.deb

ADD influx.conf /etc/influx.conf

EXPOSE 8083

EXPOSE 8086

CMD ["/opt/influxdb/influxd", "-config", "/etc/influx.conf"]
