This repository contains all source and data to explore the capabilities of the Elastic Stack with FIFA 2019 © football data.

## Dataset

See [Kaggle](data/kaggle.md).

## Elasticsearch 

Change to the `docker` directory and bring up Elasticsearch as Docker container.

```bash
docker-compose up -d
```

## Logstash

Ingest data with Logstash

```bash
docker run --rm -it \
  --network=docker_elastic-stack \
  -v $(pwd)/logstash/config/:/usr/share/logstash/config/ \
  -v $(pwd)/logstash/pipeline/:/usr/share/logstash/pipeline/ \
  -v $(pwd)/data/:/opt/data/ \
  docker.elastic.co/logstash/logstash:7.3.0
```