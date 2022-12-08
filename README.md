Repositório para armazenar os artefatos do Pipeline utilizando Modern Data Stack com AirByte + DBT + Airflow + SnowFlake + Metabase

Tarefas:

Infraestrutura:

Setup do ambiente de desenvolvimento (Hardware, Software - Linux, Python, Docker, Curl, Pip, Git, Npm, etc...) X

Setar as Permissoes do Gitpod ao Repositorio no Github X

Subir o Airbyte via docker X
    -   git clone -b modern-data-stack https://github.com/Renan-LS/airbyte.git /*URL do meu git*/
        dessa maneira, utilizando de workspace na nuvem, eu posso anexar o codigo do Airbyte a meu git, e feito isto,
        crio uma branch secundaria para poder salvar as alteracoes do ambiente AirByte e replicar em outros projetos.
    
    -   importante ressaltar que o Airbyte roda na porta 8000, E através do guia inferior ao lado do botao TERMINAL, PORTS
        consigo verificar os serviços que estao rodando em cada porta

        ps: Para verificar a relação de serviços e suas respectivas portas, bem como várias outras informaçõoes, procurar o 
        arquivo chamado docker-compose.yaml

Subir o Airflow via docker 

Subir o Metabase via docker 

Criar o script de execução 

Testar a Execução 

Snowflake Data Warehouse:

Criar a Conta no SnowFlake 
Verificar a existência das tabelas 
Obter os links de conexão e nome da conta 
Extração:

No Airbyte:

Conectar com as origens baseadas nos Csvs 
Criar as entidades no snowflake através do script base da documentação 
Conectar o destino no snowflake 
Criar as conexões do airbyte associando as origens ao destino 
Testar as conexões 
Preparação:

No Airbyte (Destination Loading Method):

Local Staging (Ambiente de Desenvolvimento) 
Cloud Staging (Ambiente de Produção) 
Transformação:

No Dbt:

Criação da Conta 
Conexão com o Github 
Criação do Dbt Project 
Criação do Profile de conexão com o snowflake 
Criação do Schema 
Criação dos Modelos Base 
Criação do Modelo Relacionado 
Visualização gráfica do modelo 

Teste de execução 
Commits, Branches, Pull Requests, Merges no Github 
Obtenção do link de conexão com o Airbyte 
Visualização:

No Metabase:

Conectar Metabase com o Snowflake
Criar uma Question
Criar um Dashboard
Adicionar uma Question
Visualizar o Resultado
Orquestração:

No Airflow:

Criar a dag

Criar a Docker network

Incluir nos composes a network criada

Setup Up no serviço

Testar a conexao entre os containers do airflow e do airbyte

Criar as conexões com o Airbyte através do script

Testar a execução do pipeline

Encerramento:

Material de Apoio:

Links

Códigos fonte

Apresentação