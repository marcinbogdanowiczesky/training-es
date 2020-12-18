# training-es

Dockerized two-nodes Elasticsearch cluster with Kibana and the following plugins installed:
- analysis-icu
- analysis-stempel
- pl.allegro.tech.elasticsearch.plugin:elasticsearch-analysis-morfologik
- ingest-attachment

## Usage
1. Build custom Elasticsearch image (with listed plugins installed):
   ```
   docker build -f elasticsearch-with-plugins -t training-es:7.9.3 .
   ```

1. \[For Windows users\] Running Docker on WSL2 requires increasing mmap counts (after every Docker/WSL2 reboot)
   ```
   wsl -d docker-desktop
   sysctl -w vm.max_map_count=262144
   ```
   Source: https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html

1. Start cluster using this command:
   ```
   docker-compose up
   ```

1. Open http://localhost:5601 in your favourite browser and start using Kibana ;-)
