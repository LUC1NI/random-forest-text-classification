# Random Forest para Classificação de Texto  

Este projeto tem como objetivo avaliar o desempenho do algoritmo **Random Forest** aplicado em três bases de dados de classificação de texto supervisionada.  

As bases de dados utilizadas foram:  
- **Amazon Cells Labelled**  
- **IMDb Reviews**  
- **Yelp Reviews**  

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

## 📂 Estrutura do Projeto  
random-forest-text-classification/
├─ notebooks/ # Jupyter Notebooks para cada base de dados
├─ report/ # Relatório consolidado com resultados
├─ data/ # (opcional) Bases de dados utilizadas
└─ README.md # Documentação do projeto

---

## 🚀 Resultados  

- O modelo apresentou boa performance nas três bases de dados, com destaque para a base **IMDb**, que obteve os melhores índices de precisão e recall.  
- A **curva ROC** mostrou separação consistente entre as classes em todos os datasets.  

*(adicione aqui prints de tabelas de métricas ou curvas ROC para enriquecer o README)*  

---

## 🛠️ Tecnologias Utilizadas  

- Python 🐍  
- Jupyter Notebook  
- Pandas / Numpy  
- Scikit-learn  
- Matplotlib / Seaborn  

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
