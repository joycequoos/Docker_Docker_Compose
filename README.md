# Docker Compose

[← Voltar a Docker](https://github.com/joycequoos/Docker/blob/main/README.md)

Docker Compose é uma ferramenta que facilita a definição e o gerenciamento de ambientes multi-contêiner. Com um arquivo YAML (`docker-compose.yml`) é possível especificar serviços, redes e volumes de uma aplicação inteira e, com um único comando (`docker-compose up`), iniciar e orquestrar todos os contêineres definidos — simplificando o desenvolvimento e a implantação de aplicações complexas.

## Índice

- [Verificando a versão instalada](#verificando-a-versão-instalada)
- [Limpando a máquina local](#limpando-a-máquina-local)
- [Download do projeto Netflix](#download-do-projeto-netflix)
- [Criando um docker-compose file](#criando-um-docker-compose-file)
- [Rodando e parando o Docker Compose](#rodando-e-parando-o-docker-compose)
- [Próximos passos](#próximos-passos)

---

## Verificando a versão instalada

Verificar a versão do Docker Compose na máquina via prompt de comando:

[![Verificar versão do Docker Compose](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/01_Verificar_Docker_Version.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/01_Verificar_Docker_Version.png)

## Limpando a máquina local

[![Limpeza geral](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/02_Limpeza_Geral.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/02_Limpeza_Geral.png)

## Download do projeto Netflix

O `docker-compose.yml` é um arquivo que contém as informações de todos os contêineres que vão subir. Neste projeto, serão criados três contêineres: um para o backend, um para o frontend e um para o banco de dados.

[![Compose backend e frontend](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/03_Compose_Back_Front.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/03_Compose_Back_Front.png)

[![Terceiro contêiner](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/04_Terceiro_Conteiner.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/04_Terceiro_Conteiner.png)

Para rodar o projeto Netflix, acessar o diretório do projeto pelo terminal e executar:

```
docker-compose up
```

[![docker-compose up](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/05_Docker_Compose_Up.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/05_Docker_Compose_Up.png)

## Criando um docker-compose file

1. Renomear o `docker-compose` de teste do projeto Netflix.

   [![Renomear docker-compose](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/06_Renomear_Docker_Compose.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/06_Renomear_Docker_Compose.png)

   > O Docker só faz a leitura do `docker-compose` mesmo quando a extensão é `.yaml`.

2. Criar o arquivo `docker-compose.yml` do zero, entendendo o passo a passo.

   [![Criando docker-compose.yml](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/07_Docker_Compose_yml.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/07_Docker_Compose_yml.png)

3. Incluir a versão do Docker Compose file. Para verificar a versão mais recente, acessar a documentação oficial:

   <https://docs.docker.com/compose/compose-file/>

   Passo a passo completo do `docker-compose.yml`:

   [![Passo a passo do docker-compose](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/08_Criando_Docker_Compose.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/08_Criando_Docker_Compose.png)

   Arquivo de exemplo completo: [`docker-compose.yml`](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/docker-compose/docker-compose.yml)

## Rodando e parando o Docker Compose

| Ação | Comando |
| --- | --- |
| Subir os contêineres em background | `docker-compose up -d` |
| Parar e remover os contêineres | `docker-compose down` |

## Próximos passos

- Adicionar variáveis de ambiente via arquivo `.env` referenciado no `docker-compose.yml`.
- Configurar volumes nomeados para persistir os dados do banco entre execuções.
- Explorar `depends_on` e healthchecks para controlar a ordem de inicialização dos serviços.
- Documentar como escalar um serviço específico com `docker-compose up --scale`.
