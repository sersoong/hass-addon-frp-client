FROM ghcr.io/home-assistant/base:3.24

ARG FRP_VERSION=0.72.0

COPY bootstrap.sh /
COPY run.sh /
COPY frpc.toml /

RUN chmod a+x /bootstrap.sh
RUN chmod a+x /run.sh

RUN /bootstrap.sh $FRP_VERSION

CMD ["/run.sh"]
