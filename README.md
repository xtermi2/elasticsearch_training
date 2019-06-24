# Elasticsearch Training

# Requirements

* docker: https://docs.docker.com/install/
* docker-compose: https://docs.docker.com/compose/install/
* postman: https://www.getpostman.com/downloads/

## startup Elasticsearch + Kibana

The vm.max_map_count kernel setting needs to be set to at least 262144: https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-cli-run-prod-mode

```bash
docker-compose up
```

You should see something like this in the logs from kibana: `Server running at http://0:5601`

Check if Elasticsearch is up an running: http://localhost:9200/_cluster/health
The response should say `"status": "green"`

Check if Kibana is up and running: http://localhost:5601 

## Prepare Postman

You should already have installed postman, now start it.

* import the collection `elasticsearch_training.postman_collection.json`

Test it and run the _00_health_check_ request. 
The response should say `"status": "green"`