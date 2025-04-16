# Relatório de Classificação de Jogos

**Nome:** Leonardo Fonseca Silva

---

## 1. Introdução

Neste trabalho, utilizei a base de dados do Steam contendo informações sobre jogos, como preço, avaliações dos jogadores, tempo médio de jogo e outros atributos relevantes. A tarefa foi classificar os jogos como **'Bom'** ou **'Ruim'**, com base em uma análise do desempenho de diferentes algoritmos de classificação. 

Foram escolhidos os algoritmos:
- Árvore de Decisão
- Random Forest
- SVM Linear
- Naive Bayes Gaussiano

Esses algoritmos foram selecionados devido às suas características de desempenho e robustez em problemas de classificação.

---

## 2. Algoritmos de Classificação

Os algoritmos implementados e comparados neste trabalho são:

### 2.1 Árvore de Decisão

Um modelo simples e interpretável que divide os dados em diferentes ramos, baseado em decisões sequenciais, até chegar a um resultado.

### 2.2 Random Forest

Uma extensão das Árvores de Decisão, composta por um conjunto de árvores independentes, gerando uma previsão com base na média das previsões de cada árvore.

### 2.3 SVM Linear

Algoritmo de classificação baseado na construção de um hiperplano que separa as classes de forma eficiente, geralmente utilizado em problemas com margens de separação bem definidas.

### 2.4 Naive Bayes Gaussiano

Modelo probabilístico baseado no teorema de Bayes, com a suposição de que as variáveis preditoras seguem uma distribuição normal.

---

## 3. Métricas de Avaliação

Para avaliar o desempenho dos modelos, utilizei as seguintes métricas:

- **Acurácia (`accuracy_score`)**: Mede a porcentagem de classificações corretas realizadas pelo modelo.
- **Matriz de Confusão (`confusion_matrix`)**: Representa o número de classificações verdadeiras e falsas para cada classe.
- **Precision, Recall e F1-Score (`classification_report`)**: Avaliam a qualidade do modelo, levando em consideração falsos positivos e negativos, bem como a taxa de acertos em relação a cada classe.

---

## 4. Comparação dos Modelos

Após a execução dos modelos, os resultados foram comparados com base nas métricas mencionadas anteriormente. A tabela a seguir apresenta uma comparação entre os modelos:

| Modelo           | Acurácia  | Precision (Bom) | Recall (Bom) | F1-score (Bom) |
|------------------|-----------|------------------|----------------|----------------|
| Árvore de Decisão| 0.976612  | 0.980429         | 0.981343       | 0.980886       |
| Random Forest    | 0.938962  | 0.930419         | 0.972948       | 0.951208       |
| SVM Linear       | 0.762122  | 0.758893         | 0.895522       | 0.821566       |
| Naive Bayes      | 0.419852  | 0.887324         | 0.058769       | 0.110236       |

> Gráfico de acurácia.

![image](https://github.com/user-attachments/assets/9080ee4e-7729-4d80-86c5-aeeffea877c2)

> Gráfico F1-Score.
> 
![image](https://github.com/user-attachments/assets/14c14bf3-d221-4bd6-8e11-de78e5bb06b4)



---

## 5. Discussão

O algoritmo **Random Forest** apresentou o melhor desempenho em termos de Acurácia, Precision, Recall e F1-Score. Isso se deve ao fato de que o Random Forest é capaz de capturar complexidades nos dados através da construção de múltiplas árvores de decisão, resultando em um modelo mais robusto.

A **Árvore de Decisão**, embora interpretável, teve um desempenho ligeiramente inferior, devido à sua tendência a overfitting em conjuntos de dados com ruído.

O **Naive Bayes**, por ser um modelo mais simples e baseado em suposições, teve o pior desempenho, mas ainda assim foi eficiente em casos com distribuições de dados mais simples.

---

## 6. Conclusão

Neste trabalho, comparei o desempenho de quatro algoritmos de classificação (Árvore de Decisão, Random Forest, SVM Linear e Naive Bayes) aplicados à base de dados de jogos do Steam.

- **Random Forest** obteve o melhor desempenho geral.
- **Árvore de Decisão** teve bom desempenho, mas com tendência a overfitting.
- **SVM Linear** apresentou bom recall, mas menor acurácia.
- **Naive Bayes** teve o pior desempenho, especialmente em Recall e F1-Score.

**Conclusão**: o **Random Forest** foi o modelo mais eficaz para essa tarefa.

---
