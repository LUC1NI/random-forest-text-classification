# 📝 Random Forest Text Classification

Este projeto tem como objetivo **classificar sentimentos em textos curtos** usando algoritmos de Machine Learning, com foco em **Random Forest**.  
Foram utilizados datasets rotulados de **reviews de produtos, restaurantes e filmes**, contendo frases positivas e negativas.

---

## 📂 Estrutura do Projeto

random-forest-text-classification/
├── data/
│   ├── amazon_cells_labelled.txt # reviews de produtos da Amazon
│   ├── imdb_labelled.txt # reviews de filmes do IMDb
│   ├── yelp_labelled.txt # reviews de restaurantes do Yelp
├── SMSbasePOC.ipynb # notebook principal com todo o pipeline
├── requirements.txt # bibliotecas necessárias
└── README.md # este arquivo

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

---

## 🚀 Como Rodar o Projeto

### 1. Clone o repositório
```bash
git clone https://github.com/LUC1NI/random-forest-text-classification.git
cd random-forest-text-classification

2. Crie o ambiente virtual e instale dependências
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

pip install -r requirements.txt

3. Execute o notebook

Abra o Jupyter Notebook e rode:

jupyter notebook SMSbasePOC.ipynb

🔍 Etapas do Projeto

Pré-processamento do texto

Conversão para minúsculas.

Remoção de pontuações e stopwords.

Vetorização usando Bag of Words.

Treinamento do modelo

Classificador Random Forest.

Avaliação

Métricas: Acurácia, Precisão, Recall e F1-score.

Comparação entre os três datasets.

📈 Resultados

O modelo Random Forest apresentou bom desempenho nos três datasets.

As métricas variaram dependendo do corpus, mas de forma geral:

IMDb → melhor recall (detecção de frases negativas).

Amazon → desempenho equilibrado entre precisão e recall.

Yelp → melhores resultados de acurácia.

🔹 Mais análises e gráficos podem ser adicionados em versões futuras.

📌 Conclusões

O projeto mostra que Random Forest é eficaz em tarefas simples de classificação de texto.

Resultados podem ser melhorados com:

Representações mais avançadas (TF-IDF, embeddings).

Comparação com outros algoritmos (Naive Bayes, Logistic Regression, SVM).

Este é um bom projeto inicial de NLP para portfólio em Data Science.

✨ Autor

👤 João Lucini (LUC1NI)

GitHub: @LUC1NI