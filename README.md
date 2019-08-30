# ElasticSearch Search Exporter
This is a simple exporter for Prometheus that executes simple search query to Elastic Search and counts amount of hits.

ElasticSearch should be installed on localhost:9200 and not credentials protected.

### ElasticSearch Query Configuration
Exporter supports multiple search queries. They can be configured in searches.json file.
Frequency of search query executtion can be set in the same file.

### Prometheus Job Configuration
```json
  - job_name: elasticsearch_search_exporter
    scrape_interval: 60s
    static_configs:
    - targets:
      - localhost:9730
```
