Repositório para armazenar os artefatos do Pipeline utilizando Modern Data Stack com AirByte + DBT + Airflow + SnowFlake + Metabase

Tarefas:

Infraestrutura:

Setup do ambiente de desenvolvimento (Hardware, Software - Linux, Python, Docker, Curl, Pip, Git, Npm, etc...) X

Setar as Permissoes do Gitpod ao Repositorio no Github X

Subir o Airbyte via docker X - PORTA 8000
    -   git clone -b modern-data-stack https://github.com/Renan-LS/airbyte.git /*URL do meu git*/
        dessa maneira, utilizando de workspace na nuvem, eu posso anexar o codigo do Airbyte a meu git, e feito isto,
        crio uma branch secundaria para poder salvar as alteracoes do ambiente AirByte e replicar em outros projetos.
    
    -   importante ressaltar que o Airbyte roda na porta 8000, E através do guia inferior ao lado do botao TERMINAL, PORTS
        consigo verificar os serviços que estao rodando em cada porta
  
        ps: Para verificar a relação de serviços e suas respectivas portas, bem como várias outras informaçõoes, procurar o 
        arquivo chamado docker-compose.yaml

Subir o Airflow via docker 8080
     -   separar por pastas os serviços

    -   Procurar "airflow docker" e abrir a documentação(sempre fazer isto)
        -  baixar o docker-compose do airflow curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.5.0/docker-compose.yaml'
        -  crir alguns arquivos que a documentação  exige 
        - depois subir um *docker compose up airflow-init*
        - agora sobe o resto dos serviços com *docker-compose up*
        - porta que vai estar disponível o serviço do AirFlow é 8080, e o usuário e senha configurados como padrão é *airflow*

            **.GITIGNORE - ARQUIVO CRIADO DENTRO DA ESTRUTURA DO PROJETO EM QUE EU DESEJO QUE AS ATUALIZAÇÕES SEJAM IGNORADAS!!****

Subir o Metabase via docker x PORTA 3001
    -   ao procurar "docker metabase" a documentação original irá me indicar a realizar a instalação do Metabase através de "docker run" fazendo com que o metabase rode em um container isolado. De modo a manter a mesma linha de arquitetura, iremos 
    fazer de maneira manual o docker-compose do Metabase, procurando no google docker-compose.yaml metabase, e criando este arquivo dentro da pasta do mesmo"
    -   copia o que achar no google e cola dentro do arquivo docker-compose.yaml , retirando a parte do postgress que não me interessa e as referencias a ele

    ps: ele pediu na aula para alterar a porta para 3000, mas deixei na que veio 3001

Criar o script de execução 

Testar a Execução 

Snowflake Data Warehouse:

Criar a Conta no SnowFlake x
Verificar a existência das tabelas x 
    -   verificar o .csv que serão usados (https://health.google.com/covid-19/open-data/raw-data)
        tabelas que serão usadas: Epidemiology , Economy

Obter os links de conexão e nome da conta x
Extração:

No Airbyte:

Conectar com as origens baseadas nos Csvs x
Criar as entidades no snowflake através do script base da documentação x
Conectar o destino no snowflake x
Criar as conexões do airbyte associando as origens ao destino x
Testar as conexões x
Preparação:

No Airbyte (Destination Loading Method):

Local Staging (Ambiente de Desenvolvimento) x
Cloud Staging (Ambiente de Produção) x



Transformação: **modelagem**

No Dbt:

Criação da Conta x
Conexão com o Github x 
Criação do Dbt Project x
    -   Nessa parte tem que realizar algumas configurações basicas no arquivo dbt_project.yml
        Criação do Profile de conexão com o snowflake 
            -cria um arquivo chamado "profiles.yaml" dentro da pasta dbt-model
        Criação do Schema x
        Criação dos Modelos Base x
Criação do Modelo Relacionado x

**todos esses passos acima estão detalhados no README.md do dbt**


Visualização gráfica do modelo x

Teste de execução x
Commits, Branches, Pull Requests, Merges no Github x 
Obtenção do link de conexão com o Airbyte x
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