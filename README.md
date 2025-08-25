# Random Forest Text Classification

Este projeto aplica TF-IDF + Random Forest em três bases de dados de classificação de texto:
Amazon, Yelp e IMDB.

## Notebooks
- notebooks/amazon.ipynb — análise da base Amazon
- notebooks/yelp.ipynb — análise da base Yelp
- notebooks/imdb.ipynb — análise da base IMDB

## Relatório
- report.md — resumo completo de todas as bases, com métricas e curvas ROC

## Como rodar
### Google Colab
1. Abra o notebook desejado
2. Faça upload do arquivo .txt correspondente
3. Execute todas as células

### Local
1. Instale as bibliotecas:
pip install -r requirements.txt

2. Abra o notebook no Jupyter
3. Coloque os arquivos .txt dentro da pasta `data/`
4. Execute todas as células
