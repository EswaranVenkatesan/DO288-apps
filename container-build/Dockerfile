# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

LABEL io.k8s.description="A basic Apache HTTP SERVER child image, uses onbuild" io.k8s.dipslay.name="APACHE HTTP SERVER" io.openshift.expose-services="8080:http" io.openshift.tags="apache, httpd"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /car/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001




