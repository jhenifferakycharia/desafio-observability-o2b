# Desafio de Observabilidade O2B Academy

## Solução para o Desafio de Observabilidade da O2B Academy
Neste repositório, você encontrará minha implementação prática para configurar um ambiente de observabilidade usando Prometheus, Grafana e Alertmanager para monitorar uma aplicação de exemplo em Python.

## Objetivo
O objetivo deste desafio era proporcionar uma experiência prática na configuração de ferramentas populares de observabilidade e entender como monitorar métricas de uma aplicação simples.

## Minha Solução

### Passos Realizados

#### Instalação do Prometheus, Grafana e Alertmanager:
- Clonei o repositório e acessei o diretório do laboratório.
- Criei um arquivo `docker-compose.yml` para definir os serviços Prometheus, Grafana e Alertmanager.

#### Configuração da Aplicação de Exemplo:
- Certifiquei-me de ter Flask e Prometheus Client Python instalados.
- Acessei o diretório da aplicação e iniciei a aplicação em Python.

#### Gerando Métricas na Aplicação:
- Acessei a aplicação em `http://localhost:3001` e cliquei em "Gerar Erro" e "Calcular Duração".

#### Configuração do Prometheus:
- No arquivo `prometheus.yml` no diretório prometheus, adicionei uma seção para coletar métricas da minha aplicação Python.

#### Integração com Webhook:
- No arquivo `alertmanager.yml` no diretório prometheus, configurei o Alertmanager para enviar alertas para o webhook site.
- Adicionei um receiver para o webhook site com o webhook URL correspondente.

#### Iniciando o Ambiente de Observabilidade:
- Voltei para o diretório raiz do projeto e executei o comando para iniciar os serviços Prometheus, Grafana e Alertmanager.

#### Acessando o Prometheus e Grafana:
- Acessei o painel do Prometheus em `http://localhost:9090` e verifiquei se estava acessando os dados da minha aplicação.
- Acessei o painel do Grafana em `http://localhost:3000` e fiz login com as credenciais padrão (admin/admin).

## Imagens:

### Prometheus

![Prometheus Targets](https://github.com/jhenifferakycharia/desafio-observability-o2b/blob/main/images/Screenshot%202023-12-30%20at%2015-20-19%20Prometheus%20Time%20Series%20Collection%20and%20Processing%20Server.png)

Configurei o Prometheus para coletar métricas da aplicação Python.

### Grafana

![Grafana Dashboard](https://github.com/jhenifferakycharia/desafio-observability-o2b/blob/main/images/Screenshot%202023-12-30%20at%2015-20-01%20lab%20observabilidade%20-%20Dashboards%20-%20Grafana.png)

O Grafana foi configurado para visualizar as métricas coletadas pelo Prometheus.

## Configuração da Aplicação

![Aplicação Web](https://github.com/jhenifferakycharia/desafio-observability-o2b/blob/main/images/Screenshot%202023-12-29%20at%2019-38-53%20Screenshot.png)

A aplicação Flask foi configurada para expor métricas ao Prometheus.

## Geração de Métricas

Utilizamos a funcionalidade da aplicação para gerar erros e calcular duração, a fim de produzir métricas para o monitoramento.

## Integração com Webhook Site

![Webhook Site](https://github.com/jhenifferakycharia/desafio-observability-o2b/blob/main/images/Screenshot%202023-12-30%20at%2015-52-01%20Webhook.site%20-%20Test%20process%20and%20transform%20emails%20and%20HTTP%20requests.png)

Integramos o Alertmanager com o Whebhook Site para receber alertas.