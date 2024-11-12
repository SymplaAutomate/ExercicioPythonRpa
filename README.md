# Exercício Prático para Desenvolvedor RPA Python

## Sobre
Este teste prático avaliará a capacidade do candidato desde a compreensão do processo a ser automatizado e documentação, até o desenvolvimento e comunicação eficaz das soluções propostas por meio de RPA.


## Objetivo:
Desenvolver um robô em Python para coletar informações sobre os estados brasileiros, suas capitais, populações e regiões. O robô deverá acessar dois conjuntos de informações, estruturar os dados, armazená-los em um banco de dados SQL e extrair estatísticas de regiões mais populosas. É necessário implementar logs para monitoramento e gerar um **Process Design Document (PDD)** que descreva o processo.

## Descrição do Processo:
O robô deverá acessar:
1. [Lista de Estados Brasileiros](https://inanyplace.blogspot.com/2017/01/lista-de-estados-brasileiros-sigla-estado-capital-e-regiao.html) para coletar informações de estados, capitais e regiões.
2. O arquivo **PopulaçãoxCapital.xlsx** para coletar as populações das capitais.

## Passos do Exercício

### 1. Extração de Dados de Estados, Capitais e Regiões:
- Acesse o primeiro link utilizando Selenium para navegar e localizar informações de estados, capitais e regiões.
- Extraia e organize as informações:
    - **Estado**: Nome do estado.
    - **Capital**: Nome da capital do estado.
    - **Região**: Nome da região onde o estado está localizado.

### 2. Leitura de População das Capitais:
- Utilize a biblioteca `pandas` para carregar os dados do arquivo **PopulaçãoxCapital.xlsx**.
- Extraia e relacione as populações com as respectivas capitais.

### 3. Estruturação e Processamento dos Dados com Pandas:
- Organize as informações extraídas em um `DataFrame` com as colunas:
    - `estado`: Nome do estado.
    - `capital`: Nome da capital.
    - `regiao`: Nome da região.
    - `populacao`: População da capital.

### 4. Armazenamento em Banco de Dados:
- Conecte-se a um banco de dados SQL (SQLite Local).
- Crie uma tabela chamada `estados` com as colunas:
    - `estado` (string)
    - `capital` (string)
    - `regiao` (string)
    - `populacao` (inteiro)
- Insira ou atualize as informações na tabela, garantindo consistência e evitando duplicações.

### 5. Consulta SQL e Exportação para CSV:
Realize uma consulta SQL para extrair as informaçoes abaixo em seus respectivos arquivos de saida.

- identificar as 3 regiões mais populosas, para:<br>`top3_regioes_populosas.csv`.
- Regioes e quantidade de capitais, para: <br>`regioes_n_capitais.xls`
- 2 estados com as capitais mais populosas, para <br> `estados_mais_populosos.xsl`

### 6. Criação de Logs:
- Registre logs para monitorar cada etapa do processo:
    - Início e conclusão da extração de dados.
    - Quantidade de registros processados e armazenados.
    - Tratamento de erros e exceções.
- Use diferentes níveis de log (INFO, WARNING, ERROR) para estruturar as mensagens de forma clara.

### 7. Geração do PDD:
- Crie um **Process Design Document (PDD)** contendo:
    - Descrição e diagrama do fluxo do processo.
    - Explicação das etapas e sub-etapas do processo.

## Fluxo Esperado:
1. Acesse o primeiro site para coletar dados de estado, capital e região com Selenium.
2. Leia o arquivo **PopulaçãoxCapital.xlsx** para coletar dados de população das capitais.
3. Estruture os dados utilizando Pandas.
4. Armazene os dados em um banco de dados SQL.
5. Realize a consulta SQL para obter o top 3 das regiões mais populosas e exporte o resultado para CSV.
6. Gere logs do processo.
7. Documente o processo em um PDD.

## Entregáveis:
- Código-fonte em um repositório Git.
- Arquivo `top3_regioes_populosas.csv` com as 3 regiões mais populosas.
- Documento PDD em PDF com o processo detalhado.

## Critérios de Avaliação:
- **Estrutura de Código**: 
    - Organização e modularidade.
    - Funcionalidade correta e completa do robô.
    - Eficiência do código.
    - Clareza e organização do código.
    - Construção de Logs.
    - Manipulação adequada de exceções e erros;
    - Boas práticas de codificação em Python;
- **Uso de Logs**: Qualidade e clareza das mensagens.
- **Resolução de Problemas**: Capacidade de lidar com erros e garantir o fluxo do processo.
- **Interação com Ferramentas**:
    - Web scraping com Selenium.
    - Manipulação de dados com Pandas.
    - Armazenamento de dados no banco SQL.
    - Extração de dados com consultas SQL.
- **Documentação**:
    - Boas Práticas na construção do PDD e SDD (material/documentação);
    - Comunicação clara, “Symples” e objetiva na apresentação do código e das documentações. 


