FROM rhel7:latest
LABEL version=1.0
LABEL maintainer="Gowrishankar Muthukrishnan <gmuthukr@redhat.com>"

COPY dist/netcontrold-0.3.el7-1.noarch.rpm ./
RUN yum install -y --enablerepo="rhel-7-fast-datapath-rpms" openvswitch && \
    yum install -y ./netcontrold-* && \
    yum clean all

ENTRYPOINT ["sh", "-c", "/usr/bin/ncd_watch"]
