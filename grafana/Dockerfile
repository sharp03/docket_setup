FROM grafana/grafana:latest
USER root
RUN apt-get update && apt-get install -y curl gettext-base && rm -rf /var/lib/apt/lists/*
#RUN yum -y update && yum -y install curl gettext-base && rm -rf /var/lib/apt/lists/*

WORKDIR /etc/grafana
COPY datasources ./datasources

WORKDIR /app
COPY entrypoint.sh ./
RUN chmod u+x entrypoint.sh

ENTRYPOINT ["/app/entrypoint.sh"]

