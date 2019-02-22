FROM multichain-2.0-beta-2-base
MAINTAINER NlaakStudiosLLC

COPY ./runchain.sh /usr/local/bin/runchain.sh
COPY ./blocknotify.sh /usr/local/bin/blocknotify.sh
RUN chmod a+x /usr/local/bin/runchain.sh
RUN chmod a+x /usr/local/bin/blocknotify.sh

EXPOSE 7447:7447
EXPOSE 8000:8000
CMD ["/bin/sh/","/usr/local/bin/runchain.sh"]
