
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
- Normalização dos dados com StandardScaler
- Avaliação com métricas de classificação
- Ajuste de threshold para melhorar o recall
- Análise da matriz de confusão

## Modelo utilizado

- Logistic Regression

## Métricas principais

Modelo inicial com threshold 0.5:

- Accuracy: 0.83
- Precision: 0.65
- Recall: 0.57
- F1-score: 0.61
- ROC-AUC: 0.83

Após ajuste de threshold para 0.3:

- Precision: 0.51
- Recall: 0.76
- F1-score: 0.61

## Comparação da matriz de confusão

Threshold 0.5:

- Falsos negativos: 159
- Verdadeiros positivos: 215

Threshold 0.3:

- Falsos negativos: 90
- Verdadeiros positivos: 284

## Conclusão

Ao reduzir o threshold de 0.5 para 0.3, o modelo aumentou o recall e passou a identificar mais clientes com risco de churn.

Essa escolha pode ser interessante em um cenário de negócio onde perder clientes é mais caro do que abordar clientes que talvez não cancelariam.

## Ferramentas utilizadas

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
