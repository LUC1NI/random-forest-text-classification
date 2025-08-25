1. Introdução
O objetivo deste trabalho é avaliar o desempenho de um classificador Random Forest aplicado a três bases de dados de classificação de texto supervisionada, contendo avaliações e mensagens anotadas com classes positivas (1) ou negativas (0).
 As bases utilizadas foram:
Amazon Cells Labelled


Yelp Labelled


IMDB Labelled


Todas possuem formato text<TAB>target e foram processadas no Google Colab, utilizando TF-IDF para vetorização dos textos.

2. Metodologia
As etapas seguidas foram:
Carregamento das bases no Colab via files.upload().


Padronização das colunas para text e target.


Análise de balanceamento das classes.


Divisão em treino (75%) e teste (25%) utilizando train_test_split.


Vetorização TF-IDF para transformar o texto em espaço vetorial.


Treinamento com RandomForestClassifier (parâmetros padrão).


Avaliação com métricas:


Accuracy (acurácia)


Precision (precisão)


Recall (revocação)


AUC (área sob a curva ROC)


Plotagem da curva ROC para análise visual do desempenho.



3. Resultados
3.1. Balanceamento das Classes
Todas as bases apresentam classes relativamente balanceadas entre positivo (1) e negativo (0), com pequenas variações.
Base
Classe 0 (%)
Classe 1 (%)
Amazon
50%
50%
Yelp
50%
50%
IMDB
48.3%
51.6%


3.2. Métricas de Avaliação
Base
Accuracy
Precision
Recall
AUC
Amazon
0.748
0.756
0.782
0.876
Yelp
0.78
0.80
0.72
0.82
IMDB
0.695
0.677
0.714
0.760


Amazon: A acurácia de 0.748 mostra que o modelo acerta em média 74,8% das previsões. A precisão de 0.756 indica que, quando o modelo prevê positivo, ele acerta cerca de 75,6% das vezes. O recall de 0.782 significa que ele consegue recuperar a maioria dos exemplos realmente positivos. Como a base é balanceada, esses valores são consistentes e não inflados artificialmente.


Yelp: Apresentou a maior acurácia (0.78), com precisão de 0.80, indicando bom desempenho ao prever positivos com baixa taxa de falsos positivos. O recall foi menor (0.72), sugerindo que alguns positivos ainda foram perdidos.


IMDB: Foi a base mais desafiadora, com acurácia menor (0.69). A precisão (0.67) indica que o modelo erra mais ao classificar positivos, e o recall (0.71) mostra que ele não recupera tão bem todos os positivos. Isso pode estar ligado ao vocabulário mais variado dos textos de filmes, o que torna a classificação mais difícil.


AUC: Em todas as bases os valores foram satisfatórios (acima de 0.75), mostrando que o modelo tem boa capacidade de separar classes positivas e negativas. O melhor resultado foi na Amazon (0.876), e o menor na IMDB (0.760), reforçando que essa última é mais complexa.

3.1. Curvas ROC

📌 Figura 1 – Curva ROC para a base Amazon

<img width="578" height="455" alt="download" src="https://github.com/user-attachments/assets/b72f7736-3351-49f8-bec6-f04e1cd64b11" />

📌 Figura 2 – Curva ROC para a base Yelp

<img width="578" height="455" alt="download" src="https://github.com/user-attachments/assets/f12f0b59-a911-42c7-9611-3c4eaa680cd0" />

📌 Figura 3 – Curva ROC para a base IMDB

<img width="578" height="455" alt="download" src="https://github.com/user-attachments/assets/1ccd666a-e7d8-4bfe-a847-3468303331d0" />



4. Conclusão
Com base nos resultados apresentados:
O modelo Random Forest apresentou desempenho consistente, com acurácia em torno de 70–78% nas três bases.


Como as classes estão balanceadas, a acurácia é confiável, ou seja, o modelo não “acerta” só porque uma classe aparece mais vezes.


A precisão mais alta (Amazon e Yelp) mostra que o modelo foi bom em evitar falsos positivos nessas bases.


O recall da Amazon foi o melhor, indicando que a base era mais previsível em termos de vocabulário. Já a IMDB foi a mais difícil, com menor precisão e recall.


A AUC confirma que, mesmo com variações, o modelo consegue separar de forma razoável as duas classes em todos os cenários.


Em resumo, o pipeline TF-IDF + Random Forest é adequado para classificação binária de textos curtos, mas o desempenho depende do tipo de vocabulário e contexto de cada base.



