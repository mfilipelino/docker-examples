# Docker

### hello world

```bash
docker containar run hello-world
```

* Download automático das imagens não encontradas: ```docker image pull```
* Criação do container: ```docker container create```
* Execução do container: ```docker container start```
* Uso do modo interativo: ```docker container exec```


## cheat-sheet

### Listar containers em execução

```bash
docker container ps
docker container ls
docker container list
docker ps
```

### Listar todos os containers

```bash
docker container ps -a
docker container ls -a 
docker container list -a 
docker ps -a
```

# rodando containers dando nome

```bash
docker container run --name mydeb  -it debian bash
```

# run container atach ao já criado pelo nome

```bash
docker container start -ai mydeb
```
# expondo a porta do serviço do container para ser acessada pelo host

```bash
docker container run -p 8080:80 nginx
docker container run -p ${PORTA_HOST}:${PORTA_CONTAINER}
```

# mapeando volumes

```bash
docker container run -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx
```

# rodando o container no modo daemon 

```bash
docker container run -d -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx
```

# status do seu container

```bash
docker container stats {NAME}
```

# start, stop and restart container

```bash
docker container stop {NAME || ID} 
docker container start {NAME || ID}
docker container restart {NAME || ID}
```

# logs do container

```bash
docker container logs {NAME}
```

# Docker inspect informações sobre o container em formato json completo.

```bash
docker container inspect {NAME}
```

# Rodar processos no seu contantainer sem acessar no modo interativo

```bash
docker container exec {name} uname -or
```


# Listar volumes que foram criados na sua maquina local

```bash
docker volumes ls 
```


## Gerenciamento de Images

# pull de imagem do registry

```bash
docker image pull {NAME:TAG}
```

# listar image

```bash
docker image ls
docker image list
```

# remover image

```bash
docker image rm {NAME | ID} 
docker rmi {NAME | ID} 
```

# inspect image

```bash
docker image inspect {NAME}
```

# create tag by image

```bash
docker image tag redis:latest redis_latest
```
--------------------------------------------------------------------------------------------------------------------------------------

# Criando suas images no docker 