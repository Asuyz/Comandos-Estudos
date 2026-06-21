# Referência Completa de Comandos do Docker CLI

> Baseado na documentação oficial (docs.docker.com), versão atual do Docker CLI.

## Containers (`docker container`)

| Comando | Atalho | Descrição |
|---|---|---|
| `docker container run` | `docker run` | Cria e inicia um novo container a partir de uma imagem |
| `docker container create` | — | Cria um container sem iniciá-lo |
| `docker container start` | — | Inicia um ou mais containers parados |
| `docker container stop` | — | Para um ou mais containers em execução |
| `docker container restart` | — | Reinicia um ou mais containers |
| `docker container pause` | — | Pausa todos os processos de um container |
| `docker container unpause` | — | Retoma os processos pausados |
| `docker container kill` | — | Mata o processo principal de um container (SIGKILL) |
| `docker container rm` | — | Remove um ou mais containers |
| `docker container ls` | `docker ps` | Lista containers |
| `docker container exec` | `docker exec` | Executa um comando em um container em execução |
| `docker container attach` | — | Conecta o terminal a um container em execução |
| `docker container logs` | — | Exibe os logs de um container |
| `docker container inspect` | — | Mostra informações detalhadas (JSON) de um container |
| `docker container top` | — | Mostra os processos em execução dentro do container |
| `docker container stats` | — | Exibe estatísticas de uso de recursos em tempo real |
| `docker container diff` | — | Mostra alterações no sistema de arquivos do container |
| `docker container cp` | — | Copia arquivos entre o container e o host |
| `docker container commit` | — | Cria uma nova imagem a partir das alterações de um container |
| `docker container export` | — | Exporta o sistema de arquivos do container como um arquivo `.tar` |
| `docker container port` | — | Lista o mapeamento de portas de um container |
| `docker container rename` | — | Renomeia um container |
| `docker container update` | — | Atualiza a configuração de recursos de um container (CPU, memória etc.) |
| `docker container wait` | — | Bloqueia até que o container pare, e retorna o código de saída |
| `docker container prune` | — | Remove todos os containers parados |

## Imagens (`docker image`)

| Comando | Atalho | Descrição |
|---|---|---|
| `docker image build` | `docker build` | Constrói uma imagem a partir de um Dockerfile |
| `docker image pull` | `docker pull` | Baixa uma imagem de um registro |
| `docker image push` | `docker push` | Envia uma imagem para um registro |
| `docker image ls` | `docker images` | Lista imagens locais |
| `docker image rm` | `docker rmi` | Remove uma ou mais imagens |
| `docker image inspect` | — | Mostra informações detalhadas de uma imagem |
| `docker image history` | — | Mostra o histórico de camadas (layers) de uma imagem |
| `docker image tag` | — | Cria uma tag para uma imagem |
| `docker image save` | — | Salva uma imagem em um arquivo `.tar` |
| `docker image load` | — | Carrega uma imagem a partir de um arquivo `.tar` |
| `docker image import` | — | Importa o conteúdo de um tarball como uma imagem |
| `docker image prune` | — | Remove imagens não utilizadas (dangling ou todas) |

## Build avançado (`docker buildx` / `docker builder`)

| Comando | Descrição |
|---|---|
| `docker buildx build` | Build estendido com suporte a multi-plataforma, cache remoto etc. |
| `docker buildx bake` | Executa builds definidos em arquivos `docker-bake.hcl`/`.json` |
| `docker buildx create` | Cria um novo builder |
| `docker buildx use` | Define o builder ativo |
| `docker buildx ls` | Lista builders disponíveis |
| `docker buildx inspect` | Mostra detalhes de um builder |
| `docker buildx rm` | Remove um builder |
| `docker buildx stop` | Para um builder |
| `docker buildx du` | Mostra uso de disco do cache de build |
| `docker buildx prune` | Remove dados de cache de build |
| `docker buildx imagetools create/inspect` | Cria/inspeciona manifests multi-arquitetura |
| `docker buildx history` | Histórico de builds (export, import, ls, logs, inspect, trace) |
| `docker buildx dial-stdio` | Expõe o builder via stdio (uso avançado/integração) |
| `docker buildx debug build` | Build com depuração interativa |
| `docker builder prune` | Remove cache de build (comando legado) |

## Rede (`docker network`)

| Comando | Descrição |
|---|---|
| `docker network create` | Cria uma nova rede |
| `docker network ls` | Lista redes |
| `docker network rm` | Remove uma ou mais redes |
| `docker network inspect` | Mostra detalhes de uma rede |
| `docker network connect` | Conecta um container a uma rede |
| `docker network disconnect` | Desconecta um container de uma rede |
| `docker network prune` | Remove redes não utilizadas |

## Volumes (`docker volume`)

| Comando | Descrição |
|---|---|
| `docker volume create` | Cria um volume |
| `docker volume ls` | Lista volumes |
| `docker volume rm` | Remove um ou mais volumes |
| `docker volume inspect` | Mostra detalhes de um volume |
| `docker volume update` | Atualiza configuração de um volume |
| `docker volume prune` | Remove volumes não utilizados |

## Docker Compose (`docker compose`)

| Comando | Descrição |
|---|---|
| `docker compose up` | Cria e inicia os containers definidos no compose file |
| `docker compose down` | Para e remove containers, redes e volumes do projeto |
| `docker compose build` | Constrói as imagens dos serviços |
| `docker compose pull` / `push` | Baixa/envia imagens dos serviços |
| `docker compose ps` | Lista containers do projeto |
| `docker compose logs` | Mostra logs dos serviços |
| `docker compose exec` | Executa um comando em um serviço em execução |
| `docker compose run` | Executa um serviço pontualmente (one-off) |
| `docker compose start/stop/restart` | Controla o ciclo de vida dos serviços |
| `docker compose pause/unpause` | Pausa/retoma serviços |
| `docker compose kill` | Força a parada dos serviços |
| `docker compose rm` | Remove containers parados do projeto |
| `docker compose config` | Valida e exibe a configuração final do compose |
| `docker compose convert` | Converte o compose file para outro formato |
| `docker compose cp` | Copia arquivos entre host e serviço |
| `docker compose create` | Cria containers sem iniciar |
| `docker compose events` | Transmite eventos em tempo real |
| `docker compose export` | Exporta o sistema de arquivos de um container do serviço |
| `docker compose images` | Lista imagens usadas pelos serviços |
| `docker compose ls` | Lista projetos compose em execução |
| `docker compose port` | Mostra a porta pública de um serviço |
| `docker compose publish` | Publica a definição do projeto em um registro |
| `docker compose scale` | Ajusta o número de réplicas de um serviço |
| `docker compose stats` | Estatísticas de uso de recursos dos serviços |
| `docker compose top` | Processos em execução nos serviços |
| `docker compose volumes` | Lista volumes do projeto |
| `docker compose wait` | Bloqueia até a saída dos serviços |
| `docker compose watch` | Observa alterações e sincroniza/reconstrói automaticamente |
| `docker compose bridge convert` | Converte compose file para manifests do Kubernetes |
| `docker compose alpha *` | Comandos experimentais (`dry-run`, `scale`, `watch`) |

## Swarm e orquestração

**`docker swarm`**: `init`, `join`, `join-token`, `leave`, `unlock`, `unlock-key`, `update`, `ca`

**`docker node`**: `ls`, `inspect`, `promote`, `demote`, `ps`, `rm`, `update`

**`docker service`**: `create`, `ls`, `inspect`, `ps`, `logs`, `rm`, `rollback`, `scale`, `update`

**`docker stack`**: `deploy`, `ls`, `ps`, `rm`, `services`, `config`

## Sistema (`docker system`)

| Comando | Descrição |
|---|---|
| `docker system info` | Informações gerais do ambiente Docker |
| `docker system df` | Uso de disco (imagens, containers, volumes, cache) |
| `docker system events` | Transmite eventos em tempo real do daemon |
| `docker system prune` | Remove dados não utilizados (containers, redes, imagens, cache) |

## Comandos de topo de nível (atalhos diretos)

Esses são atalhos para os comandos de gerenciamento acima, e funcionam diretamente em `docker <comando>`:

`run`, `ps`, `pull`, `push`, `images`, `exec`, `build`, `login`, `logout`, `search`, `info`, `version`, `inspect`, `init`

## Segurança e confiança

**`docker trust`**: `inspect`, `sign`, `revoke`, `key generate`, `key load`, `signer add`, `signer remove`

**`docker secret`** (Swarm): `create`, `inspect`, `ls`, `rm`

**`docker config`** (Swarm): `create`, `inspect`, `ls`, `rm`

**`docker manifest`**: `create`, `annotate`, `inspect`, `push`, `rm`

**`docker pass`**: `get`, `set`, `ls`, `rm` (gerencia segredos no keychain local do SO)

**`docker scout`**: análise de vulnerabilidades e SBOM — `cves`, `quickview`, `compare`, `recommendations`, `sbom`, `policy`, `environment`, `repo enable/disable/list`, `attestation add/get/list`, `cache df/prune`, `watch`, `stream`, `vex get`, `integration configure/list/delete`, `enroll`, `config`

## Contextos e plugins

**`docker context`**: `create`, `use`, `ls`, `inspect`, `rm`, `update`, `show`, `export`, `import`

**`docker plugin`**: `install`, `enable`, `disable`, `create`, `inspect`, `ls`, `push`, `rm`, `set`, `upgrade`

**`docker checkpoint`**: `create`, `ls`, `rm` (snapshots de estado de containers, recurso experimental)

## Docker Desktop

**`docker desktop`**: `start`, `stop`, `restart`, `status`, `update`, `logs`, `diagnose`, `version`, `enable`/`disable model-runner`, `engine ls/use`, `kubernetes images`

## IA e MCP (recursos mais recentes)

**`docker model`** (Docker Model Runner — execução local de LLMs): `run`, `pull`, `push`, `list`, `rm`, `inspect`, `ps`, `logs`, `status`, `bench`, `df`, `package`, `tag`, `search`, `show`, `skills`, `requests`, `unload`, `purge`, `gateway`, `context create/inspect/ls/rm/use`, `*-runner` (install, start, stop, restart, reinstall, uninstall)

**`docker mcp`** (gerenciamento de servidores/clientes MCP): `catalog`, `client`, `feature`, `gateway run`, `profile`, `secret`, `server init`, `tools`

**`docker dhi`** (Docker Hardened Images): `catalog`, `attestation`, `auth apk`, `customization`, `mirror`

**`docker sandbox`** (ambientes isolados para agentes de IA como Claude, Codex, Gemini etc.): `create`, `run`, `exec`, `ls`, `inspect`, `stop`, `rm`, `reset`, `save`, `network log/proxy`

**`docker offload`**: `start`, `stop`, `status`, `diagnose`, `version` (offload de builds/execução para a nuvem da Docker)

**`docker debug`**: shell de depuração para qualquer container ou imagem, alternativa ao `docker exec`

## Outros

| Comando | Descrição |
|---|---|
| `docker init` | Gera arquivos iniciais (Dockerfile, compose) para um projeto |
| `docker version` | Mostra a versão do cliente e do daemon |
| `docker info` | Detalhes do ambiente Docker (igual a `system info`) |
| `docker login` / `logout` | Autentica/desautentica em um registro |
| `docker search` | Busca imagens no Docker Hub |

---

### Observações práticas

A forma moderna recomendada é usar os comandos com namespace explícito (`docker container ls`, `docker image rm` etc.) em vez dos atalhos legados (`docker ps`, `docker rmi`), já que a Docker vem sinalizando a possibilidade de ocultar os atalhos legados no futuro via `DOCKER_HIDE_LEGACY_COMMANDS`.

Para ver as flags de qualquer comando: `docker <comando> --help`.

Fonte: [docs.docker.com/reference/cli/docker](https://docs.docker.com/reference/cli/docker/)