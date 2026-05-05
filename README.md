
# Churn Prediction - Telco Customer Churn

Projeto de Machine Learning para prever cancelamento de clientes (churn) utilizando dados da base Telco Customer Churn.

## Objetivo

Identificar clientes com maior probabilidade de cancelamento, permitindo que a empresa atue com estratégias de retenção.

## Etapas do projeto

- Limpeza e preparação dos dados
- Tratamento de valores ausentes
- Conversão de variáveis categóricas
- Separação entre treino e teste com estratificação
- Treinamento de modelo de Regressão Logística
- Ajuste de threshold para melhorar o recall
- Treinamento de modelo Random Forest
- Comparação entre modelos
- Análise da matriz de confusão

## Modelos utilizados

- Logistic Regression
- Random Forest

## Resultados dos modelos

### Logistic Regression - Threshold 0.5

- Accuracy: 0.83
- Precision: 0.65
- Recall: 0.57
- F1-score: 0.61
- ROC-AUC: 0.83

### Logistic Regression - Threshold 0.3

- Precision: 0.51
- Recall: 0.76
- F1-score: 0.61

### Random Forest

- Accuracy: 0.79
- Precision: 0.63
- Recall: 0.49
- F1-score: 0.55
- ROC-AUC: 0.82

## Comparação das matrizes de confusão

### Logistic Regression - Threshold 0.5

- Falsos negativos: 159
- Verdadeiros positivos: 215

### Logistic Regression - Threshold 0.3

- Falsos negativos: 90
- Verdadeiros positivos: 284

### Random Forest

- Falsos negativos: 190
- Verdadeiros positivos: 184

## Conclusão

Neste projeto, o principal objetivo era identificar clientes com maior risco de churn.

A Regressão Logística com threshold ajustado para 0.3 apresentou o melhor recall, identificando mais clientes com risco de cancelamento.

O Random Forest foi testado como comparação, mas neste primeiro experimento teve recall menor e deixou passar mais clientes que realmente cancelaram.

Por isso, considerando o objetivo de negócio, a melhor opção até o momento foi a Regressão Logística com threshold 0.3.

## Ferramentas utilizadas

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
