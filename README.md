# log-management

A common solution for log management using the Elastic Stack.

## What is the Elastic Stack?

Elastic Stack refers to Beats, Elasticsearch, Logstash and Kibana, is the most popular open source logging platform.

## Brief Introduction of each Components

- Beats: data shippers, send data from logs to Logstash or Elasticsearch directly. Using Filebeat in this repo
- Elasticsearch: distributed search engine with schema-free JSON documents
- Logstash: data processing pipeline, ingest data, transforms it and sends it to Elasticsearch
- Kibana: visualize data in Elasticsearch

## Sources of Logs

1. Regular script scan database in specific time interval, executed once a hour. Generate log files in json format, Filebeat scan local logs directory and ship to Logstash
2. Filebeat deploys in the service image, each service executes its own logic and generates logs in the format of protocols, ship to Logstash on server

