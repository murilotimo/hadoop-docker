Este respoitório foi baseado (neste repositório)[https://github.com/sequenceiq/hadoop-docker]
# Aquela Tecnologia Hadoop 2.9.1 Docker image

[![DockerPulls](https://img.shields.io/docker/pulls/aquelatecnologia/hadoop.svg)](https://registry.hub.docker.com/u/aquelatecnologia/hadoop/)
[![DockerStars](https://img.shields.io/docker/stars/aquelatecnologia/hadoop.svg)](https://registry.hub.docker.com/u/aquelatecnologia/hadoop/)


# Criando a imagem

Para criar a sua imagem a partir do Dockerfile, basta executar o seguinte comando 

```
docker build  -t aquelatecnologia/hadoop:2.9.1 .
```

# Baixe a imagem (ainda não disponível)

```
docker pull aquelatecnologia/hadoop:2.9.1
```

# Iniciar um container

Para iniciar a imagem que você criou ou fez o pull, basta usar o seguinte comando:

```
docker run -it aquelatecnologia/hadoop:2.9.1 /etc/bootstrap.sh -bash
```

ou

```
docker-compose up -d
```

## Testando

Para testar o hadoop, basta executar o seguinte comando dentro do container:

```
hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-2.9.1.jar grep input output 'dfs[a-z.]+'

# verificar a saída
hdfs dfs -cat output/*
```
