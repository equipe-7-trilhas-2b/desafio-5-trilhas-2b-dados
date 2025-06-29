# Projeto Dashboard Power BI - Análise de Queimadas no Maranhão (2025)

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-orange?logo=microsoft-power-bi&logoColor=white)](https://powerbi.microsoft.com/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![GitHub](https://img.shields.io/badge/GitHub-Versioning-black?logo=github&logoColor=white)](https://github.com/)

## Descrição do Projeto

Este projeto tem como objetivo a construção de um dashboard interativo no Power BI para análise e comunicação dos resultados relacionados às queimadas no estado do Maranhão, no ano de 2025. Através de visualizações claras e intuitivas, busca-se facilitar a tomada de decisões e o entendimento dos padrões, tendências e anomalias presentes nos dados.

## Estrutura do Repositório

```plaintext
.
├── README.md
├── dashboard
│   └── dash-prevfogo.pbix                          # Arquivo do dashboard Power BI publicado no serviço
├── data
│   ├── processed
│   │   └── queimadas_MA_2025_clean_v20250628.csv   # Dados tratados para análise
│   └── raw
│       └── focos_mensal_ma_2025.csv                # Dados brutos originais
├── notebooks
│   ├── 01_data_cleaning.ipynb                      # Notebook para limpeza e preparação dos dados
│   └── 02_data_eda.ipynb                           # Notebook de Análise Exploratória dos Dados (EDA)
└── requirements.txt                                # Dependências do ambiente Python para análise
```

## Coleta e Preparação dos Dados

* **Fonte dos dados:** Dados coletados de fontes oficiais e confiáveis, contendo registros mensais dos focos de queimadas no Maranhão em 2025.
* **Tratamento:**

  * Padronização de formatos de datas e variáveis.
  * Remoção de duplicidades e inconsistências.
  * Tratamento de valores ausentes para garantir integridade.
  * Dados limpos armazenados na pasta `data/processed` para análises.
* Todo o processo está documentado e reproduzível no notebook [`notebooks/01_data_cleaning.ipynb`](notebooks/01_data_cleaning.ipynb).

## Análise Exploratória dos Dados (EDA)

* Aplicação de técnicas para identificar padrões sazonais, distribuição geográfica, tendências e outliers.
* Resultados detalhados no notebook [`notebooks/02_data_eda.ipynb`](notebooks/02_data_eda.ipynb).
* Uso de gráficos, tabelas e métricas descritivas para fundamentar o dashboard.
* Paleta de cores suaves e acessíveis, com foco na experiência do usuário.
* Filtros interativos permitem exploração dinâmica por município, período e outras dimensões.

## Definição e Aplicação de KPIs e Visões do Dashboard

O dashboard foi estruturado em três visões principais para facilitar a análise multidimensional dos dados de queimadas no Maranhão, cada uma destacando KPIs estratégicos que refletem aspectos essenciais dos incidentes monitorados:

### 1. Visão Geral dos Incidentes

Esta página oferece uma síntese abrangente da situação atual dos focos de queimadas:

* **Total de Incidentes:** Quantidade acumulada de focos registrados até o momento (ex.: 34.791).
* **Mês com Mais Incidentes:** Identificação do mês com maior número de focos, destacando a sazonalidade temporal (ex.: Junho).
* **FRP Máximo Registrado:** Valor máximo do Fire Radiative Power (FRP), indicador da intensidade do fogo (ex.: 1234,10).
* **Distribuição por Bioma:** Gráfico circular detalhando a proporção dos incidentes em cada bioma (Cerrado, Amazônia, Caatinga).
* **Incidentes por Município:** Ranking dos municípios com maior número de focos, facilitando a identificação das áreas mais críticas.
* **Tendência Temporal:** Gráfico de área exibindo a evolução dos incidentes ao longo dos meses, permitindo rápida visualização de picos e quedas.

### 2. Análise Temporal com Sazonalidades

Foco na compreensão dos padrões temporais e sazonais dos focos de queimadas:

* **Hora com Mais Incidentes:** Período do dia com maior ocorrência dos focos (ex.: 16h).
* **Dia da Semana com Mais Incidentes:** Identificação do dia da semana mais crítico (ex.: Quarta-feira).
* **FRP Médio:** Valor médio do Fire Radiative Power, refletindo a intensidade típica das queimadas.
* **Incidentes por Semana do Mês:** Distribuição dos focos considerando a semana do mês para identificar padrões intra-mensais.
* **Incidentes por Dia da Semana:** Visualização do comportamento semanal dos incidentes.
* **Incidentes por Período do Dia:** Segmentação dos incidentes entre manhã, tarde e noite, com gráficos de fácil interpretação.

### 3. Análise Geográfica

Proporciona insights espaciais para apoiar decisões locais e regionais:

* **Incidentes por Município:** Média dos incidentes calculada por município, oferecendo uma métrica consolidada.
* **Média de Dias Sem Chuva:** Indicador meteorológico fundamental para análise do risco e comportamento dos focos.
* **Média do FRP por Município:** Valor médio do FRP em cada município, indicando a severidade local das queimadas.
* **Mapa dos Incidentes:** Visualização geoespacial detalhada com pontos representando a localização dos focos, destacando regiões críticas no Maranhão, incluindo os biomas Amazônia, Caatinga e Cerrado.

## Dashboard Power BI

- Arquivo principal: `dashboard/dash-prevfogo.pbix`  
- Publicado no Power BI Service, disponível em:  
  [Acessar Dashboard no Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiOTFlZTQ3NTEtYTkzZS00YzM1LTkwYjktYmE3Y2UwZWIxYTA0IiwidCI6IjVlZjU2ZTRmLTA0MjEtNGJlOS04YzZmLTVlZDkwMzdhZDZjZiJ9)

## Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/equipe-7-trilhas-2b/desafio-5-trilhas-2b-dados.git
   cd desafio-5-trilhas-2b-dados
   ```

2. Crie e ative o ambiente virtual:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Execute os notebooks para exploração dos dados:

   ```bash
   jupyter notebook
   ```

5. Para visualizar o dashboard localmente, abra o arquivo:

   ```
   dashboard/dash-prevfogo.pbix
   ```

   ou acesse a versão publicada no Power BI Service (link acima).