FROM docker.elastic.co/elasticsearch/elasticsearch:5.1.2

ADD elasticsearch.yml /usr/share/elasticsearch/config/

USER root
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml

# elasticsearch cannot be executed by 'root' user for security reasons
# Details: https://discuss.elastic.co/t/why-is-it-elasticsearch-is-not-allowed-to-run-as-root/60413
USER elasticsearch
