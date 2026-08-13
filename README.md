# Docker Compose

Docker Compose é uma ferramenta que facilita a definição e o gerenciamento de ambientes de conteineres Docker. Ele permite que você defina e configure um aplicativo multi-contêiner em um arquivo YAML ('docker-compose.yml'), especificando os serviços, redes e volumes necessários para sua aplicação. Com um único comando ('docker-compose up'), você pode iniciar e orquestrar todos os contêineres definidos no arquivo, simplicando o desenvolvimento e a implatação de aplicativos complexos.

- Verificando a versão do docker compose na maquina via prompt de comando.

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/01_Verificar_Docker_Version.png">

### 01. Limpando a maquina local

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/02_Limpeza_Geral.png">

### 02. Download projeto Netflix

- O docker compose é um arquivo que contem as informações de todos os conteiners que vão subir, onde vamos criar um conteiner para backend, um segundo conteiner para frontend e um terceiro conteiner para Banco de Dados.

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/03_Compose_Back_Front.png">

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/04_Terceiro_Conteiner.png">

02.01 Rodando o projeto Netflix, acessar o diretorio do projeto netflix pelo terminal, e colocar o comando docker-compose up

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/05_Docker_Compose_Up.png">

### 03. Criando um docker compose file

03.01 - Renomear o docker-compose para teste do projeto Netflix

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/06_Renomear_Docker_Compose.png">

- O Docker só realiza a leitura de docker-compose mesmo quando a extensão é .yaml

03.02 - Criando o arquivo docker-compose.yml, para fazermos a construção do 0, entendendo o passo a passo.

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/07_Docker_Compose_yml.png">

03.03 - Primeiro passo incluir a versão do docker compose file, para verificar a mais recente acessar a documentação:

https://docs.docker.com/compose/compose-file/

- Passo a passo do Docker-Compose

<img src="https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/img/08_Criando_Docker_Compose.png">

https://github.com/JosiTubaroski/Docker_Docker_Compose/blob/main/docker-compose/docker-compose.yml

### 4 - Rodando e parando o docker compose

4.1 - Subindo o conteiner

docker-compose up -d

4.2 - Parando o conteiner

docker-compose down
