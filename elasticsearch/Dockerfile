FROM docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.4

ADD ./config/ /usr/share/elasticsearch/config/

EXPOSE 9200
EXPOSE 9300

VOLUME /usr/share/elasticsearch/data
