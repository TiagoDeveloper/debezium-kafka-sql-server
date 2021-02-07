# Introduction 
TODO: Give a short introduction of your project. Let this section explain the objectives or the motivation behind this project. 


## Comandos básicos do docker-compose (Os comandos terão que serem executados na pasta onde se encontra o arquivo docker-compose.yml)
- Comando para subir os containers
  ```
  docker-compose up --build -d
  ```
  NOTA: a flag ```-d``` é opcional e é para que os logs dos containers sejam listados em background.
  A  flag ```--build``` é obrigatória após a a primeira vez que os container com seus respectivos volumes são criados, sendo que sua obrigatoriedade pode voltar, nos casos em que os volumes sejam deletados.
- Comando para listar os logs dos containers docker-compose
  ```
  docker-compose logs
  ```
## Comandos básicos do docker
- Comando para listar todas as imagens
  ```
  docker image ls
  ```
- Comando para listar todos os containers
  ```
  docker ps
  ```
- Comando para listar todos os volumes
  ```
  docker volume ls
  ```
- Comando para parar um determinado container
  ```
  docker stop <CONTAINER ID>
  ```
## Comandos básicos de interação do docker com container (Específicos para os cotainer do Kafka)
- Comando para entrar dentro dos containers relacionados ao ambiente kafka
  ```
  docker exec -it <CONTAINER ID> bash
  ```
## Comandos básicos do kafka
- Visualizar as mensagens criadas pelo Debezium
  ```
  docker exec <CONTAINER ID DO KAFKA> /kafka/bin/kafka-console-consumer.sh \
  --bootstrap-server <IP DO KAFKA>:9092 \
  --from-beginning \
  --property print.key=true \
  --topic <NOME DO TOPICO>
  ```
## Ferramentas UI do kafka
- [Ferramenta desktop para conectar ao kafka chamada _kaDeck_](https://www.getkadeck.com/#/)
- [Ferramenta desktop para conectar ao kafka chamada _Conduktor_](https://www.conduktor.io/download/)
## Infográfico do ambiente kafka com o plugin debezium: 
![alt text](https://s3.amazonaws.com/imagens-hml.araujo.com.br/apresentacao_debezium_kafka.jpg "migração de dados sql server para postgresql")



## FONTES
- https://www.infoq.com/br/articles/apache-kafka-ksqldb/

