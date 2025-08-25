# 📊 Relatório – Classificação de Texto com Random Forest

## 1. Introdução
O objetivo deste trabalho é avaliar o desempenho de um **classificador Random Forest** aplicado a três bases de dados de **classificação de texto supervisionada**, contendo avaliações e mensagens anotadas com classes **positivas (1)** ou **negativas (0)**.  

As bases utilizadas foram:  
- **Amazon Cells Labelled**  
- **Yelp Labelled**  
- **IMDB Labelled**  

Todas possuem formato `text<TAB>target` e foram processadas no **Google Colab**, utilizando **TF-IDF** para vetorização dos textos.

---

## 2. Metodologia
As etapas seguidas foram:

1. **Carregamento das bases** no Colab via `files.upload()`.  
2. **Padronização das colunas** para `text` e `target`.  
3. **Análise de balanceamento** das classes.  
4. **Divisão** em treino (75%) e teste (25%) utilizando `train_test_split`.  
5. **Vetorização TF-IDF** para transformar o texto em espaço vetorial.  
6. **Treinamento** com `RandomForestClassifier` (parâmetros padrão).  
7. **Avaliação** com métricas:
   - Accuracy (acurácia)  
   - Precision (precisão)  
   - Recall (revocação)  
   - AUC (área sob a curva ROC)  
8. **Plotagem da curva ROC** para análise visual do desempenho.  

---

## 3. Resultados

### 3.1. Balanceamento das Classes
Todas as bases apresentam classes relativamente balanceadas entre positivo (1) e negativo (0), com pequenas variações.

| Base   | Classe 0 (%) | Classe 1 (%) |
|--------|-------------|--------------|
| Amazon | 50%         | 50%          |
| Yelp   | 50%         | 50%          |
| IMDB   | 48.3%       | 51.6%        |

---

### 3.2. Métricas de Avaliação

| Base   | Accuracy | Precision | Recall | AUC   |
|--------|----------|-----------|--------|-------|
| Amazon | 0.748    | 0.756     | 0.782  | 0.876 |
| Yelp   | 0.780    | 0.800     | 0.720  | 0.820 |
| IMDB   | 0.695    | 0.677     | 0.714  | 0.760 |

- **Amazon**:  
  A acurácia de **0.748** mostra que o modelo acerta em média 74,8% das previsões.  
  A precisão de **0.756** indica que, quando o modelo prevê positivo, ele acerta 75,6% das vezes.  
  O recall de **0.782** mostra que consegue recuperar a maioria dos exemplos realmente positivos.  

- **Yelp**:  
  Apresentou a **maior acurácia (0.78)**, com precisão de **0.80**, indicando bom desempenho ao prever positivos com baixa taxa de falsos positivos.  
  O recall menor (**0.72**) sugere que alguns positivos foram perdidos.  

- **IMDB**:  
  Foi a base mais desafiadora, com acurácia de **0.69**.  
  A precisão (**0.67**) indica maior erro ao classificar positivos, e o recall (**0.71**) mostra que o modelo não recupera tão bem todos os positivos.  
  Isso pode estar ligado ao vocabulário mais variado dos textos de filmes.  

- **AUC**:  
  Em todas as bases os valores foram satisfatórios (acima de **0.75**), mostrando que o modelo tem boa capacidade de separar classes positivas e negativas.  
  Melhor resultado: **Amazon (0.876)**.  
  Pior resultado: **IMDB (0.760)**.  

---

### 3.3. Curvas ROC

📌 **Figura 1 – Curva ROC para a base Amazon**  
<img width="578" height="455" alt="ROC Amazon" src="https://github.com/user-attachments/assets/b72f7736-3351-49f8-bec6-f04e1cd64b11" />

📌 **Figura 2 – Curva ROC para a base Yelp**  
<img width="578" height="455" alt="ROC Yelp" src="https://github.com/user-attachments/assets/f12f0b59-a911-42c7-9611-3c4eaa680cd0" />

📌 **Figura 3 – Curva ROC para a base IMDB**  
<img width="578" height="455" alt="ROC IMDB" src="https://github.com/user-attachments/assets/1ccd666a-e7d8-4bfe-a847-3468303331d0" />

---

## 4. Conclusão
Com base nos resultados apresentados:  

- O modelo **Random Forest** apresentou desempenho consistente, com acurácia entre **70% e 78%**.  
- Como as classes estão **balanceadas**, a acurácia é confiável, sem viés por distribuição.  
- A precisão mais alta (Amazon e Yelp) mostra que o modelo foi eficaz em **evitar falsos positivos**.  
- O **recall da Amazon** foi o melhor, indicando que essa base era mais previsível em termos de vocabulário.  
- A **IMDB foi a mais difícil**, devido à maior variedade de termos.  
- A **AUC confirma** que o modelo separa bem as classes, mesmo com variações entre bases.  

📌 **Resumo**: O pipeline **TF-IDF + Random Forest** é adequado para classificação binária de textos curtos, mas o desempenho depende fortemente do vocabulário e do contexto de cada dataset.

---
