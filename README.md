
# Análise da Criminalidade no Brasil em 2022 e sua Relação com Fatores Sociais

Este projeto tem como objetivo analisar a criminalidade no Brasil no ano de 2022, utilizando o número de homicídios como principal indicador, e investigar como ela se relaciona com fatores sociais como educação, desemprego, renda per capita e saúde, a nível municipal.

## Objetivos
- Coletar dados de homicídios por município no Brasil (ano de 2022).
- Coletar dados sociais de educação, saúde, renda per capita e desemprego.
- Consolidar os dados em um único dataframe.
- Realizar análise exploratória e identificar possíveis correlações.
- Aplicar modelos estatísticos (como regressão linear múltipla) para quantificar relações.
- Apresentar visualizações interativas e mapas temáticos.
- Criar um banco de dados na nuvem (AWS) para armazenamento dos dados tratados e conexão direta com o Power BI.

## Fontes de Dados
- Homicídios: Atlas da Violência (IPEA) ou DataSUS.
- Educação, Renda, Saúde: Atlas Brasil 2022 (www.atlasbrasil.org.br).
- Desemprego: IBGE - PNAD Contínua.

## Estrutura do Projeto
```
data/
    ├── raw/               # Dados brutos coletados
    ├── processed/         # Dados tratados e prontos para análise
notebooks/
    ├── coleta_dados.ipynb # Coleta e organização dos dados
    ├── eda.ipynb          # Análise exploratória (gráficos, correlações)
    ├── modelagem.ipynb    # Modelagem estatística (regressões)
src/
    ├── utils.py           # Funções auxiliares para coleta e limpeza
outputs/
    ├── figures/           # Imagens e gráficos gerados
    ├── mapas/             # Mapas temáticos
infra/
    ├── aws_setup.md       # Documentação da infraestrutura na AWS
docs/
    ├── relatorio_aprendizagem.tex # Notas de aprendizado e documentação
```

## Ferramentas Utilizadas
- Python 3.11
- Pandas, NumPy, Matplotlib, Seaborn
- Geopandas e Folium (para mapas)
- Scikit-learn (para modelagem)
- PostgreSQL (RDS AWS)
- Power BI (conectado ao banco na nuvem)
- Jupyter Notebook
- VSCode + WSL2 + Conda

## Status do Projeto
Em desenvolvimento.
