FROM influxdb:1.8.10

LABEL author="Alexis Le Provost <alexis.leprovost@outlook.com>"
LABEL version="1.0.0"
LABEL description="InfluxDB1.x docker image"

USER root

ADD ./influxdb.template.conf /influxdb.template.conf
RUN mkdir -p /usr/share/collectd/
ADD ./types.db /usr/share/collectd/types.db 


ADD run.sh /run.sh
ENTRYPOINT ["bash", "/run.sh"]
