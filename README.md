# desafio-engenharia-de-dados

Repositório de instrução do desafio para vaga de Engenharia de Dados na SMTR.

## Descrição do desafio

Neste desafio você deverá capturar, estruturar e armazenar dados de uma
API instantânea. A API consiste nos dados de GPS do BRT que são gerados
na hora da consulta com o último sinal transmitido por cada veículo.

Para o desafio, será necessário construir uma pipeline que captura os
dados minuto a minuto e gera um arquivo no formato CSV. O arquivo gerado
deverá conter no mínimo 2 horas de dados capturados - estruture os dados
da maneira que achar mais conveniente. Porfim, deve ser feito o upload
do arquivo CSV para o Google Cloud Storage na mesma pipeline. Passos
extras podem ser desenvolvidos e estão indicados na seção [Etapas](#etapas)

A pipeline deverá ser construída subindo uma
instância local do [Prefect](https://github.com/PrefectHQ/prefect) com o
uso do Docker Agent (em Python).

- **O desafio deve ser entregue num repositório público do Github, com o link
enviado por email até 13/12 (ter) às 23:59 (horário de Brasília)**
- **O código enviado será testado localmente, portanto
organize e documente suas etapas.**

## Etapas

1. Instalar e configurar o
   [Prefect Server](https://docs.prefect.io/orchestration/getting-started/install.html)
   locamente com o [Docker Agent](https://docs.prefect.io/orchestration/agents/docker.html)
2. Construir a pipeline de captura da [API do
   BRT](http://citgisbrj.tacom.srv.br:9977/gtfs-realtime-exporter/findAll/json)
   com os dados minuto a minuto.
3. Gerar arquivo no formato CSV contendo 2 horas de captura e enviar para o
   Google Cloud Storage (link do bucket enviado por email).
4. (extra) Particionar tabela gerada da forma que achar mais conveniente
5. (extra) Criar view no Google BigQuery a partir dos dados salvos no Storage

## Dicas

- Teste a consistência de seus dados e evite duplicações de capturas.
- Caso realize alguma transformação nos dados originais, documente de forma
  que esteja claro o que foi feito.
- Para fazer a conexão com o Google Cloud Storage e BigQuery, você pode utilizar
  o pacote da
  [basedosdados](https://basedosdados.github.io/mais/reference_api_py/).

## Dúvidas?

Entre em contato por email :)