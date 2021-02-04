# debezium-kafka-sql-server
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
