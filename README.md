Projeto de engenharia de dados : MODERN-DATA-STACK

Se utilizando de um ambiente de desenvolvimento online, foi elaborado uma pipeline para tratamento de dados extraídos do Google Open data a respeito do Covid-19, alocados em um DW e posteriormente tratados de modo a gerar e modelar uma nova fonte de dados, apenas com as informações mais relevantes (escolhidas ao acaso), simulando um processo completo de Extração, carregamento e tratamento de dados (ELT).

As tabelas extraídas da fonte primária de dados foram: Economy, Demographics, Index e Epidemiology. A tabela final contendo os dados extraídos e tratados é a covid19_model.

Através do Airflow foi possível a criação de DAGs para que a atualização dos dados fosse diária.


Tecnologias Utilizadas:

    -   GITPOD: Workspace
    -   Airbyte: Ferramenta de ETL/ELT
    -   Airflow: Orquestração
    -   Snowflake: Data Warehouse
    -   DBT: Transformação e modelagem de dados
    -   Metabase: Apresentação dos dados
    -   Base de dados utilizada : https://health.google.com/covid-19/open-data/raw-data
