# Análise de Séries Temporais: Razão de População vs Número de Empresas por Região

Este projeto tem como objetivo realizar uma análise da série temporal da razão entre a população em uma faixa etária específica (38-58 anos) e o número de empresas no mercado imobiliário de diversas regiões do Brasil. A análise considera o período de 2007 a 2020, com previsões para os anos de 2021 e 2022, e utiliza o modelo ARIMA para prever a evolução dessa razão em diferentes regiões.

## Objetivo

- Estudar a evolução da razão entre a população de 38 a 58 anos e o número de empresas no setor imobiliário em 5 regiões do Brasil.
- Prever essa razão para os anos de 2021 e 2022.
- Identificar quais regiões estão mais saturadas e quais têm maiores oportunidades para o futuro.
  
## Passos do Projeto

### 1. Coleta de Dados

#### Dados de Empresas
Os dados sobre o número de empresas ativas por região entre 2007 e 2020 foram extraídos via a API do SIDRA, utilizando requisições HTTP. A tabela utilizada foi a **Tabela 1757** - Dados gerais das empresas de construção, segundo as faixas de pessoal ocupado.

#### Dados de População
Os dados de população, especificamente da faixa etária de 38 a 58 anos, foram extraídos da **Projeção da População** disponibilizada pelo IBGE, em formato Excel/ODS. A interpolação foi utilizada para ajustar as faixas etárias para o intervalo necessário.

### 2. Processamento de Dados

A partir dos dados obtidos, as séries temporais de número de empresas e de população foram ajustadas para que se relacionassem de forma a calcular a razão entre a população de 38 a 58 anos e o número de empresas ativas.

### 3. Análise Exploratória

A análise exploratória de dados foi feita para identificar padrões e comportamentos nas séries temporais. Gráficos de linha, correlações e estatísticas descritivas foram gerados para facilitar a compreensão da evolução dos dados.

### 4. Modelagem e Previsões para 2021 e 2022 com ARIMA

O modelo ARIMA foi ajustado para cada região considerando a série temporal da razão entre a população e o número de empresas. Com os modelos ARIMA ajustados, foram feitas previsões para os anos de 2021 e 2022 para cada região. As previsões fornecem uma estimativa da razão entre a população de 38 a 58 anos, utilizando também as estimativas de número de empresas e população. O modelo é avaliado usando o erro quadrático médio (RMSE - Root Mean Squared Error). Esse valor indica o quão bem o modelo foi capaz de prever os dados de 2019 e 2020.

### 5. Análise dos Resultados

Os resultados da análise exploratória e previsões foi possível identificar:
- Regiões mais saturadas (maior número de empresas em comparação com a população).
- Regiões com maiores oportunidades futuras (onde a razão entre a população e o número de empresas está mais favorável para crescimento).

### Conclusão
  
  O projeto utiliza o modelo ARIMA para prever a razão entre população e número de empresas nas cinco regiões do Brasil para 2021 e 2022. O uso de modelos de séries temporais e a análise do erro de previsão ajudam a fornecer insights valiosos sobre o crescimento das empresas em relação à população ao longo dos anos. As visualizações geradas ajudam a compreender as tendências para cada região, destacando as previsões futuras.

- As previsões revelam que as regiões **Sudeste** e **Sul** apresentam as menores razões para os anos de 2021 e 2022, o que indica uma maior saturação do mercado nessas regiões.
- As regiões **Norte** e **Nordeste** parecem ter maiores oportunidades para o crescimento, com uma razão mais baixa entre a população e o número de empresas.

## Dependências

- **Python 3.x**: A versão recomendada para o ambiente Python.
- **Bibliotecas**:
  - `pandas`: Para manipulação e análise de dados.
  - `numpy`: Para operações matemáticas.
  - `matplotlib`, `seaborn`: Para visualização de dados.
  - `statsmodels`: Para modelagem ARIMA e análise estatística.
  - `requests`: Para fazer chamadas HTTP para a API do SIDRA.
  - `pandas` para leitura de arquivos Excel.
  - `scipy`: Para realizar o testes ADF e correlação.


### **Estrutura do Repositório**

/projeto-imobiliario
│
├── /data
│   ├── raw
│   │   ├── pop.xlsx
│   ├── processed
│   │   ├── pronto.csv
│
├── /notebooks
│   ├── coleta_tratamento.ipynb
│   ├── eda.ipynb
│   ├── modelo.ipynb
│
├── README.md
├── requirements.txt
```



