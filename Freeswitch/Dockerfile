FROM develbro/dev:freeswitch
LABEL maintainer="Aleksey Maksimov"

#RUN apt-get -y --quiet update \
#    && apt-get -y --quiet --force-yes install freeswitch-all festvox-ru \
#    && cp -a /usr/share/freeswitch/conf/vanilla /etc/freeswitch \
#    && rm -rf /usr/share/freeswitch/conf \
#    && mkdir -p /docker-entrypoint.d /certs /db /recordings /scripts /var/lib/freeswitch /var/run/freeswitch \
#    && apt-get clean && rm -rf /var/lib/apt/lists/*

ENV LANG en_US.utf8

COPY docker-entrypoint.sh /
COPY freeswitch /etc/freeswitch

VOLUME /tts_files

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["freeswitch"]
