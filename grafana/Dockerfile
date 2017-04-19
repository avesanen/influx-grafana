FROM ubuntu:14.04

RUN apt-get update
RUN apt-get install -y wget adduser libfontconfig

RUN wget https://s3-us-west-2.amazonaws.com/grafana-releases/release/grafana_4.2.0_amd64.deb 
RUN sudo dpkg -i grafana_4.2.0_amd64.deb

ENTRYPOINT ["/usr/sbin/grafana-server", "--config=/etc/grafana/grafana.ini", "--homepath=/usr/share/grafana", "cfg:default.paths.data=/grafana/data", "cfg:default.paths.logs=/grafana/log"]

