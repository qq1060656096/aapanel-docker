FROM aapanel/aapanel:lnmp

USER root

RUN yum -y update
RUN mv /www/server/panel/pyenv/lib/python3.7/site-packages/OpenSSL /tmp/OpenSSL_bak
RUN btpip install pyOpenSSL


RUN chmod -R +x /www/server/panel
RUN chmod -R 777 /www

# Update AAPanel
RUN bt 16

WORKDIR /www/
