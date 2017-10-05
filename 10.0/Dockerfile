FROM odoo:10.0
MAINTAINER Jesus Zapata <chuchocorleone@gmail.com>

USER root

# Mount  /mnt/addons for users addons
RUN mkdir -p /mnt/addons \
        && chown -R odoo /mnt/addons
VOLUME ["/mnt/addons"]

# Set default user when running the container
USER odoo

ENTRYPOINT ["/entrypoint.sh"]
CMD ["odoo"]
