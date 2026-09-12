# Docker Compose

[← Back to Docker](https://github.com/joycequoos/Docker/blob/main/README.md)

Docker Compose is a tool that makes it easier to define and manage multi-container environments. With a YAML file (`docker-compose.yml`), you can specify the services, networks, and volumes of an entire application, and with a single command (`docker-compose up`), start and orchestrate all the defined containers — simplifying the development and deployment of complex applications.

## Table of Contents

- [Checking the Installed Version](#checking-the-installed-version)
- [Cleaning Up the Local Machine](#cleaning-up-the-local-machine)
- [Downloading the Netflix Project](#downloading-the-netflix-project)
- [Creating a docker-compose File](#creating-a-docker-compose-file)
- [Running and Stopping Docker Compose](#running-and-stopping-docker-compose)
- [Next Steps](#next-steps)

---

## Checking the Installed Version

Check the Docker Compose version on the machine via the command prompt:

[![Check Docker Compose version](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/01_Verificar_Docker_Version.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/01_Verificar_Docker_Version.png)

## Cleaning Up the Local Machine

[![General cleanup](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/02_Limpeza_Geral.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/02_Limpeza_Geral.png)

## Downloading the Netflix Project

`docker-compose.yml` is a file that contains the information for all the containers that will be started. In this project, three containers will be created: one for the back end, one for the front end, and one for the database.

[![Compose back end and front end](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/03_Compose_Back_Front.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/03_Compose_Back_Front.png)

[![Third container](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/04_Terceiro_Conteiner.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/04_Terceiro_Conteiner.png)

To run the Netflix project, go to the project directory in the terminal and run:

```
docker-compose up
```

[![docker-compose up](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/05_Docker_Compose_Up.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/05_Docker_Compose_Up.png)

## Creating a docker-compose File

1. Rename the Netflix project's test `docker-compose` file.

   [![Rename docker-compose](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/06_Renomear_Docker_Compose.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/06_Renomear_Docker_Compose.png)

   > Docker only reads `docker-compose` when the extension is `.yaml`.

2. Create the `docker-compose.yml` file from scratch, understanding it step by step.

   [![Creating docker-compose.yml](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/07_Docker_Compose_yml.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/07_Docker_Compose_yml.png)

3. Include the Docker Compose file version. To check the latest version, check the official documentation:

   <https://docs.docker.com/compose/compose-file/>

   Complete step-by-step of the `docker-compose.yml`:

   [![Step-by-step of docker-compose](https://github.com/joycequoos/Docker_Docker_Compose/raw/main/img/08_Criando_Docker_Compose.png)](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/img/08_Criando_Docker_Compose.png)

   Complete sample file: [`docker-compose.yml`](https://github.com/joycequoos/Docker_Docker_Compose/blob/main/docker-compose/docker-compose.yml)

## Running and Stopping Docker Compose

| Action | Command |
| --- | --- |
| Start the containers in the background | `docker-compose up -d` |
| Stop and remove the containers | `docker-compose down` |

## Next Steps

- Add environment variables via a `.env` file referenced in `docker-compose.yml`.
- Set up named volumes to persist database data between runs.
- Explore `depends_on` and healthchecks to control the startup order of services.
- Document how to scale a specific service with `docker-compose up --scale`.
