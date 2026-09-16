# O que é Docker?
Serviço de Virtualização

<br>

## Porque usar o Docker?
Soluciona o clássico problema: "na minha máquina funciona"

<br>

## Máquina Virtual vs Docker
Uma máquina virtual (VM) virtualiza o hardware inteiro e roda um sistema operacional completo, enquanto o Docker virtualiza o sistema operacional e compartilha o kernel da máquina hospedeira
<img width="654" height="297" alt="image" src="https://github.com/user-attachments/assets/ec0cd180-99d6-462b-9a28-4366e53ef1dc" />

<br>

## Comandos básicos 
  Visualizar a versão:
  
    docker --version
    
    docker compose --version

  Criar uma imagem e rodar:

    docker build -t teste .

  Rodar um container a partir da imagem:

    docker run teste

  Rodar em background (modo detached):

    docker run -d teste

  Rodar mapeando uma porta (host:container):

    docker run -p 8080:80 teste

<br>

## Listando imagens e containers

  Ver imagens criadas:

    docker images

  Ver containers em execução:

    docker ps

  Ver todos os containers, incluindo os parados:

    docker ps -a

<br>

## Removendo imagens e containers

  Remover um container:

    docker rm nome_ou_id

  Remover um container em execução (forçado):

    docker rm -f nome_ou_id

  Remover uma imagem:

    docker rmi nome_ou_id

<br>

## Executando comandos dentro de um container

  Abrir um terminal dentro do container:

    docker exec -it nome_ou_id sh

  Ver os logs do container:

    docker logs nome_ou_id

<br>

## Dockerfile

O Dockerfile é o arquivo que define como a imagem será construída, passo a passo.

Exemplo básico:

    FROM alpine:latest
    WORKDIR /app
    COPY . .
    CMD ["echo", "Funcionou!"]

<br>

## Docker Compose

Usado para orquestrar múltiplos containers ao mesmo tempo, através de um arquivo `docker-compose.yml`.

  Subir os serviços definidos:

    docker compose up

  Subir em background:

    docker compose up -d

  Parar e remover os serviços:

    docker compose down

<br>

## Limpeza do ambiente

  Remover containers, redes e cache não utilizados:

    docker system prune

  Ver o espaço ocupado pelo Docker:

    docker system df

  
