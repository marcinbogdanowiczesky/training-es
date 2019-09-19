# training-es

Dockerized two-nodes Elasticsearch cluster with Kibana and the following plugins installed:
- analysis-icu
- analysis-stempel
- ~~pl.allegro.tech.elasticsearch.plugin:elasticsearch-analysis-morfologik~~ (not available yet)
- ingest-attachment

## Usage
1. Build custom Elasticsearch image (with listed plugins installed):
   ```
   docker build -f elasticsearch-with-plugins -t training-es:7.3.1 .
   ```
2. Start cluster using this command:
   ```
   docker-compose up
   ```
3. Open http://localhost:5601 in your favourite browser and start using Kibana ;-)
