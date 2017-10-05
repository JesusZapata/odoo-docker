FROM odoo:10.0
MAINTAINER Jesus Zapata <chuchocorleone@gmail.com>

USER root

# Copy entrypoint script and Odoo configuration file
COPY ./odoo.conf /etc/odoo/
RUN chown odoo /etc/odoo/odoo.conf

# Mount  /mnt/addons for users addons
RUN mkdir -p /mnt/addons \
        && chown -R odoo /mnt/addons
VOLUME ["/mnt/addons"]

# Set default user when running the container
USER odoo

ENTRYPOINT ["/entrypoint.sh"]
CMD ["odoo"]
