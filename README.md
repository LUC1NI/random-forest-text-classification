# 📝 Random Forest Text Classification

Este projeto tem como objetivo **classificar textos em categorias** usando algoritmos de Machine Learning, com foco em **Random Forest**.  
É um projeto voltado para aprendizado em **Data Science** e demonstração em portfólio.

---

## 📂 Estrutura do Projeto

```shell
random-forest-text-classification/
│── data/
│ ├── amazon_cells_labelled.txt # reviews de produtos da Amazon
│ ├── imdb_labelled.txt # reviews de filmes do IMDb
│ ├── yelp_labelled.txt # reviews de restaurantes do Yelp
├─ notebooks/
│ ├── amazon_cells_labelled.ipynb
│ ├── imdb_labelled.ipynb
│ ├── yelp_labelled.ipynb
├─ report/
│ ├── report.md
│── requirements.txt # bibliotecas necessárias
│── README.md # este arquivo
```

Cada base contém textos anotados como **positivo (1)** ou **negativo (0)**.  

---

## 📊 Metodologia  

1. **Pré-processamento dos dados**  
   - Limpeza de texto (remoção de stopwords, pontuação e normalização).  
   - Vetorização utilizando **TF-IDF**.  

2. **Treinamento**  
   - Algoritmo: **Random Forest Classifier**.  
   - Divisão dos dados em treino e teste.  

3. **Avaliação**  
   - Métricas utilizadas:  
     - **Acurácia**  
     - **Precisão**  
     - **Recall**  
     - **F1-Score**  
   - Curva ROC para visualização da performance.  

---

## 📊 Dataset
Foram utilizados três datasets de **sentiment analysis** do repositório **UCI Machine Learning**:  
- **Amazon** – Opiniões sobre produtos eletrônicos.  
- **IMDb** – Avaliações de filmes.  
- **Yelp** – Reviews de restaurantes.  

Cada dataset contém **1000 frases rotuladas** (500 positivas e 500 negativas).

---

## ⚙️ Tecnologias Utilizadas
- Python 3.x
- Bibliotecas:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`


## 🚀 Resultados  

- O modelo apresentou boa performance nas três bases de dados, com destaque para a base **IMDb**, que obteve os melhores índices de precisão e recall.  
- A **curva ROC** mostrou separação consistente entre as classes em todos os datasets.  

*(adicione aqui prints de tabelas de métricas ou curvas ROC para enriquecer o README)*  

---


## 📌 Como Executar  

1. Clone o repositório:  
   ```bash
   git clone https://github.com/LUC1NI/random-forest-text-classification.git
   
Acesse a pasta:

cd random-forest-text-classification

Abra os notebooks no Jupyter ou Google Colab e execute as células.

👤 Autor
João Lucini

Estudante de Análise e Desenvolvimento de Sistemas

Interesse em Python, SQL, Power BI e Machine Learning

LinkedIn | GitHub
