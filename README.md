# Análise estatística e previsão de resultados no futebol europeu: um projeto de ciência de dados end-to-end

O futebol é uma paixão mundial e, por trás das emoções em campo, existem números que contam histórias, revelam padrões e até antecipam resultados. Neste projeto, proponho uma abordagem end-to-end de ciência de dados, aplicando coleta, limpeza, análise exploratória, modelagem preditiva e visualização de dados com foco no futebol europeu.

## Objetivo
- Coletar dados históricos de campeonatos europeus (Premier League, La Liga, Bundesliga, Serie A e Ligue 1) utilizando APIs e datasets públicos.
- Realizar uma análise exploratória profunda, identificando padrões de desempenho de times e jogadores, distribuição de gols por tempo de jogo, efeito do mando de campo, entre outros fatores.
- Criar um modelo preditivo simples para estimar o resultado de partidas futuras, baseado em estatísticas históricas e dados recentes.
- Apresentar os resultados em dashboards e visualizações interativas.

## Ferramentas e Tecnologias
- **Linguagens:** Python  
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Requests, JSON, Jupyter  
- **Fontes de dados:**  
   - Understat API (dados de xG, partidas e times)  
   - Football-data.co.uk (dados históricos)  
   - Kaggle (dados complementares)  
- **Ambiente de desenvolvimento:** WSL2 + Conda + VSCode  
- **Visualização final:** Notebook interativo e dashboards (com possibilidade de expandir para Streamlit)

## O que é o environment.yml?
O arquivo `environment.yml` é um documento gerado a partir do ambiente Conda atual, que contém todas as dependências e configurações usadas no projeto. Isso permite que qualquer pessoa recrie exatamente o mesmo ambiente em sua máquina usando apenas esse arquivo, com o comando:

```
conda env create -f environment.yml
```

## Entrega final
- Relatório exploratório completo em notebook.
- Scripts Python organizados na pasta `src/`.
- Dashboard visual (inicialmente em notebook; possibilidade de criar uma interface Streamlit).
- Repositório completo no GitHub, com `README.md` descritivo e ambiente exportado (`environment.yml`).

