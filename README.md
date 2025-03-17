# Executar SQL Server 2022 em Container Docker

## Pré-requisitos
- Docker Desktop instalado ([Download Docker](https://www.docker.com/products/docker-desktop))
- Docker Compose (já incluído no Docker Desktop)

## Configuração Inicial

1. Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:


# .env

SQL_PASSWORD=SqlServer2025
SQL_PORT=1433
SQL_DATA_PATH=./data
SQL_BACKUP_PATH=./backup


## Executar o Container ##
# First remove the existing container
docker rm -f Sql_learning

# Then recreate your container
docker-compose up -d

## Verificar Status

docker-compose ps

## Parar o Container

docker-compose down

## Recriar o Container (após alterações)

docker-compose up -d --force-recreate

## Acesso ao SQL Server

- Host: localhost:
- Usuário: sa
- Senha: SqlServer2025

## Diretórios Mapeados

- ./data : Armazena os arquivos de banco de dados
- ./backup : Local para armazenar backups .bak