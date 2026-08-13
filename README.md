# Containers

[← Voltar a Docker](https://github.com/joycequoos/Docker/blob/main/README.md)

Comandos essenciais para gerenciar contêineres no dia a dia: nomear, ver logs, mapear portas, executar comandos internos, iniciar, parar e remover contêineres.

## Índice

- [Nomeando contêineres](#nomeando-contêineres)
- [Verificando o log de eventos](#verificando-o-log-de-eventos)
- [Publicando portas de acesso](#publicando-portas-de-acesso)
- [Executando comandos em contêineres](#executando-comandos-em-contêineres)
- [Iniciando e parando contêineres](#iniciando-e-parando-contêineres)
- [Removendo contêineres](#removendo-contêineres)
- [Próximos passos](#próximos-passos)

---

## Nomeando contêineres

1. Listar os contêineres em execução na máquina. No prompt de comando, com o Docker em execução:

   ```
   docker ps
   ```

   [![Lista de contêineres](https://github.com/joycequoos/Docker_Containers/raw/main/img/01_Lista_Containers.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/01_Lista_Containers.png)

2. Criar um contêiner a partir de uma imagem (em background) com um nome específico.

   [![Nomeando contêineres](https://github.com/joycequoos/Docker_Containers/raw/main/img/02_Nomeando_Conteiners.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/02_Nomeando_Conteiners.png)

   [![Contêiner criado](https://github.com/joycequoos/Docker_Containers/raw/main/img/03_Container_Criado.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/03_Container_Criado.png)

## Verificando o log de eventos

1. Opções disponíveis para analisar logs de contêineres.

   [![Logs de contêineres](https://github.com/joycequoos/Docker_Containers/raw/main/img/04_Logs_Containers.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/04_Logs_Containers.png)

2. Usando a opção `-f` para acompanhar os logs em tempo real.

   [![docker logs -f](https://github.com/joycequoos/Docker_Containers/raw/main/img/05_docker_logs_F.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/05_docker_logs_F.png)

3. Usando o timestamp para verificar os logs.

   [![docker logs -t](https://github.com/joycequoos/Docker_Containers/raw/main/img/06_docker_logs_t.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/06_docker_logs_t.png)

## Publicando portas de acesso

1. Mapeando portas — tudo que chegar na porta 80 do computador será redirecionado para a porta 3000 do Docker.

   [![Mapeando portas](https://github.com/joycequoos/Docker_Containers/raw/main/img/07_Mapeando_Portas.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/07_Mapeando_Portas.png)

2. Aplicação em execução.

   [![Acessando aplicação](https://github.com/joycequoos/Docker_Containers/raw/main/img/08_Acessando_Aplicacao.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/08_Acessando_Aplicacao.png)

3. Contêiner criado com o nome incluído.

   [![Contêiner com mapeamento de portas](https://github.com/joycequoos/Docker_Containers/raw/main/img/09_App_Map_Ports.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/09_App_Map_Ports.png)

4. Verificando as portas do contêiner por comando.

   [![docker ps com mapeamento de portas](https://github.com/joycequoos/Docker_Containers/raw/main/img/10_Docker_ps_MapPorts.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/10_Docker_ps_MapPorts.png)

## Executando comandos em contêineres

Verificando os arquivos dentro do contêiner, a partir do terminal da máquina:

[![Comando ls dentro do contêiner](https://github.com/joycequoos/Docker_Containers/raw/main/img/11_Comandos_ls.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/11_Comandos_ls.png)

> **Observação:** sempre usar `docker exec <nome_do_conteiner> <comando>`.

## Iniciando e parando contêineres

1. Parando um contêiner que está em execução.

   [![docker stop](https://github.com/joycequoos/Docker_Containers/raw/main/img/12_Docker_Stop.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/12_Docker_Stop.png)

2. Iniciando um contêiner que está parado.

   [![docker start](https://github.com/joycequoos/Docker_Containers/raw/main/img/13_Docker_Start.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/13_Docker_Start.png)

## Removendo contêineres

[![docker rm](https://github.com/joycequoos/Docker_Containers/raw/main/img/14_Docker_Rm.png)](https://github.com/joycequoos/Docker_Containers/blob/main/img/14_Docker_Rm.png)

## Próximos passos

- Praticar `docker exec -it <nome_do_conteiner> sh` para abrir um shell interativo dentro do contêiner.
- Explorar `docker inspect` para ver detalhes completos de configuração de um contêiner.
- Automatizar a limpeza de contêineres parados com `docker container prune`.
- Testar volumes (`-v`) para persistir dados entre reinícios de contêiner.
