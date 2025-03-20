# 📊 Análise estatística e previsão de resultados no futebol europeu: um projeto de ciência de dados end-to-end

O futebol é uma paixão mundial e, por trás das emoções em campo, existem números que contam histórias, revelam padrões e até antecipam resultados. Neste projeto, proponho uma abordagem end-to-end de ciência de dados, aplicando coleta, limpeza, análise exploratória, modelagem preditiva e visualização de dados com foco na Premier League.

## Objetivo
- Coletar dados históricos da Premier League utilizando a API do Understat e datasets públicos.
- Realizar uma análise exploratória profunda, identificando padrões de desempenho de times e jogadores, distribuição de gols por tempo de jogo, efeito do mando de campo, entre outros fatores.
- Fazer um estudo específico da temporada 2018/2019, caracterizada pela disputa acirrada entre Manchester City e Liverpool, analisando o crescimento das pontuações desses clubes como funções lineares e comparando com o comportamento das curvas de pontuação dos demais times.
- Criar um modelo preditivo simples para estimar o resultado de partidas futuras, baseado em estatísticas históricas e dados recentes.
- Apresentar os resultados em dashboards e visualizações interativas.

## Ferramentas e Tecnologias
- **Linguagens:** Python  
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Requests, JSON, Jupyter  
- **Fontes de dados:**  
   - Understat API (dados de xG, partidas e times)  
   - Football-data.co.uk (dados históricos complementares)  
- **Ambiente de desenvolvimento:** WSL2 + Conda + VSCode  
- **Visualização final:** Notebook interativo e dashboards (com possibilidade de expandir para Streamlit)

## Estrutura inicial do projeto
- `data/raw/`: dados coletados da API ou arquivos CSV originais  
- `data/processed/`: dados tratados e prontos para modelagem  
- `notebooks/`: análises exploratórias, coleta e modelagem  
- `src/`: scripts Python auxiliares  

## Notebook inicial: coleta de dados
O notebook `notebooks/coleta_dados.ipynb` inclui:

### 1. Importação de bibliotecas essenciais
```python
import requests
import json
import pandas as pd
import os
```

### 2. Função para acessar a API do Understat
```python
def get_understat_data(league: str, season: str):
    url = f"https://understat.com/league/{league}/{season}"
    response = requests.get(url)
    if response.status_code != 200:
        raise Exception(f"Erro ao acessar {url}")
    return response.text
```

### 3. Coleta automatizada de temporadas da Premier League
```python
seasons = ['2018', '2019']  # Foco inicial nas temporadas 2018/2019
league = 'EPL'  # English Premier League

os.makedirs("../data/raw", exist_ok=True)

for season in seasons:
    data = get_understat_data(league, season)
    with open(f"../data/raw/understat_{league}_{season}.json", "w") as f:
        f.write(data)
    print(f"Temporada {season} coletada com sucesso!")
```

### 4. Visualização básica inicial
- Exibição da evolução de pontuação dos times rodada a rodada na temporada 2018/2019.
- Análise comparativa da linearidade das curvas de pontuação de Manchester City e Liverpool versus outros clubes.

## Entrega inicial
- Notebook `coleta_dados.ipynb` pronto para execução.
- Dados brutos salvos localmente.
- Repositório completo no GitHub, com `README.md` e ambiente exportado (`environment.yml`).

