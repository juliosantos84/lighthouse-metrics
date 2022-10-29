FROM prom/prometheus
RUN mkdir -p /prometheus/targets
ADD scrape-targets.json /prometheus/targets/scrape-targets.json
ADD prometheus.yml /etc/prometheus/
ENTRYPOINT [ "/bin/prometheus" ]
CMD        [ "--web.listen-address=127.0.0.1:9090", \
    "--config.file=/etc/prometheus/prometheus.yml", \
    "--storage.tsdb.path=/prometheus", \
    "--web.console.libraries=/usr/share/prometheus/console_libraries", \
    "--web.console.templates=/usr/share/prometheus/consoles" ]
