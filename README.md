# Projeto de engenharia de dados : MODERN-DATA-STACK

Se utilizando de um ambiente de desenvolvimento online, foi elaborado uma pipeline para tratamento de dados extraídos do Google Open data a respeito do Covid-19, alocados em um DW e posteriormente tratados de modo a gerar e modelar uma nova fonte de dados, apenas com as informações mais relevantes (escolhidas ao acaso), simulando um processo completo de Extração, carregamento e tratamento de dados (ELT).

Data Source: https://health.google.com/covid-19/open-data/raw-data

As tabelas extraídas da fonte primária de dados foram: Economy, Demographics, Index e Epidemiology. A tabela final contendo os dados extraídos e tratados é a covid19_model, conforme figura abaixo:
![tabelas](https://user-images.githubusercontent.com/120025497/207059147-0e6add3e-5969-4caa-985c-71fc01414516.jpg)



Através do DBT, foi criado a modelagem conforme o esquema abaixo, alem de ter sido realizado as junções e alguns tratamentos básicos como a transformação das tuplas NaN em 0.
![modelo](https://user-images.githubusercontent.com/120025497/207059701-0d65109a-ab4a-4c37-bf3b-98c7bf1c3a8e.jpg)



Após extraídos, carregados em um DW e tratados, os dados agora poderão ser utilizadas para posterior extração de Insights pelos interessados, de acordo com sua necessidade. Abaixo segue um simples exemplo de exposição dos dados resultantes do processo realizado por este projeto.
![metabase](https://user-images.githubusercontent.com/120025497/207061349-a86107cb-88e7-4ded-9280-0a79c368c92f.jpg)


Abaixo segue as ferramentas utilizadas neste trabalho, bem como uma ilustração do pipeline completo.

    -   GITPOD: Workspace
    -   Airbyte: Ferramenta de ETL/ELT
    -   Airflow: Orquestração
    -   Snowflake: Data Warehouse
    -   DBT: Transformação e modelagem de dados
    -   Metabase: Apresentação dos dados
    
![pipeline](https://user-images.githubusercontent.com/120025497/207061621-b42c2666-041f-4486-b5a9-6db76ac006b1.jpg)



