# Databases

- Postgres
  - IP: 192.10.1.1
- MySql
  - IP: 192.10.1.2
- Mongo
  - IP: 192.10.1.3
- Mongo Express
  - IP: http://localhost:27080
- Redis
  - IP: 192.10.1.5
- RabbitMq
  - IP: 192.10.1.6


# Softwares

- Spark
  - IP: 192.10.1.7


## Install


```sh
$ git clone https://github.com/williamsouzaa/my-databases-docker.git
$ cd my-databases-docker
$ docker compose up -d
$ docker compose ps
```

## Execute pyspark

```bash
docker exec -t pyspark spark-submit /home/Projects/{file}
```