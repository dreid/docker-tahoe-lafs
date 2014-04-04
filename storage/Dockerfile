FROM dreid/tahoe-lafs-base

# /etc/tahoe.cfg.tmpl used by tahoe-setup
ADD tahoe.cfg /etc/tahoe.cfg.tmpl

RUN tahoe create-node -p none /tahoe

# port 34567 specified in tahoe-setup
EXPOSE 34567

ADD tahoe-setup /usr/local/bin/tahoe-setup
RUN chmod +x /usr/local/bin/tahoe-setup

ENTRYPOINT /usr/local/bin/tahoe-setup


