# Network traffic analysis with elasticsearch-ntopng-kibana

Instruct ntopng to save port mirrored traffic Elasticsearch for customised reports using an "ENK" stack (Elasticsearch-ntopng-Kibana).

Ntopng allows you to export monitoring data do external sources. For low-traffic sites, SQLite and the ntopng historical interface can be a good option. As your traffic increases you are forced to put your data on a database if you care about performance and long-term data persistency. 
 In ES parlance an index is what a table is on a relational database. In order to avoid putting all data in a single index (ES can harvest old data with you by configuring the data retention), ntopng will create a daily index automatically for you by using the index name specified on the command line. By default (unless you configure it) ES does not use a password to protect data, so you can leave the password field blank. Make sure that you do not change the /_bulk/ URL as ES likes it that way (of course you can change the host name and port).

Once started, ntopng will push ES flows that are expired or periodically send (every 5 mins) partial flows for long lasting flows. By connecting to Kibana using a web browser you can immediately start seeing incoming flows appear in realtime.

A brief introduction of ntopng,  Elasticsearch and Kibana

# Ntopng
ntopng is the next generation version of the original ntop, a network traffic probe that monitors network usage. ntopng is based on libpcap and it has been written in a portable way in order to virtually run on every Unix platform, MacOSX and on Windows as well.

  https://i0.wp.com/www.ntop.org/wp-content/uploads/2015/06/Screen-Shot-2015-06-03-at-12.33.11.png?ssl=1
  https://i0.wp.com/www.ntop.org/wp-content/uploads/2015/06/Screen-Shot-2015-06-03-at-12.37.27.png?ssl=1

# Elasticsearch
Elasticsearch is an open source search engine based on Lucene, developed in Java. It provides a distributed and multitenant full-text search engine with an HTTP Dashboard web-interface (Kibana). The data is queried, retrieved and stored with a JSON document scheme. Elasticsearch is a scalable search engine that can be used to search for all kind of text documents, including log files.

  https://www.elastic.co/downloads/elasticsearch

# Kibana
Kibana is an open source data visualization tool for Elasticsearch. Kibana provides a pretty dashboard web interface. It allows you to manage and visualize data from Elasticsearch. It's not just beautiful, but also powerful.

  https://www.elastic.co/downloads/kibana

# Dashboards
 
Visualizations can be created and seen in Dashboard section. Moreover custom made dashboard has been uploaded in json format.


