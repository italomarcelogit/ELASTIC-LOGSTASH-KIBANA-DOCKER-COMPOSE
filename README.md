# ELASTIC-LOGSTASH-KIBANA-DOCKER-COMPOSE
## Enviroments ELK (ElasticSearch, logstash e Kibana) clusterizado com docker-compose

Example of docker containers in an ELK environment.

This example demonstrates how to monitor the temperature of cold cameras in different locations in Brazil.

Steps:
- start docker service
- docker-compose up # in your directory

- test environment
    - ELASTIC => http://localhost:9200/
    - LOGSTASH => http://localhost:9600/
    - KIBANA => http://localhost:5608/
    
- access you kibana url and create index template (template is kibana directory)

- test environment, by curl command
    curl -XPOST --header "Content-Type: application/json" "http://localhost:8080/" -d '{"cidade":"Recife","estacao":"CAMERA_FRIA_K01-PE","latitude":-8,"leitura":3,"longitude":-35,"sensor_id":9,"time":1614567960000,"uf":"PE"}'
    make script that it generate many json logs changing: 
      - cidade (city)
      - estacao (site)
      - latitude
      - longitude
      - leitura (value from temperature from cold clambers site)
      - sensor_id (auto increment)
      - time (unix datetime hour and minute)
      - uf: (region or state from city)
 
 - access kibana and create index pattern
 
 - create your visualizes and dashboards
 
 Good luck.
 My contact: https://www.linkedin.com/in/italomarcelo/
