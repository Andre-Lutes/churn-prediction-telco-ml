
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
- Ajuste de parâmetros do Random Forest
- Comparação entre modelos
- Análise da matriz de confusão
- Análise de importância das variáveis

## Modelos utilizados

- Logistic Regression
- Logistic Regression com threshold ajustado
- Random Forest
- Random Forest ajustado

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

### Random Forest Ajustado

- Accuracy: 0.75
- Precision: 0.52
- Recall: 0.79
- F1-score: 0.62
- ROC-AUC: 0.84

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

### Random Forest Ajustado

- Falsos negativos: 79
- Verdadeiros positivos: 295

## Variáveis mais importantes

Com o modelo Random Forest, também foi analisada a importância das variáveis.

As principais variáveis identificadas foram:

- TotalCharges
- tenure
- MonthlyCharges
- Contract_Two year
- PaymentMethod_Electronic check
- InternetService_Fiber optic
- Contract_One year
- OnlineSecurity_Yes
- gender_Male
- TechSupport_Yes

Essas variáveis indicam que o churn está relacionado principalmente ao tempo de permanência do cliente, valores pagos, tipo de contrato, método de pagamento e serviços contratados.

## Conclusão

Neste projeto, o principal objetivo era identificar clientes com maior risco de churn.

Após os testes, o melhor resultado até o momento foi obtido com o Random Forest ajustado.

Esse modelo apresentou o maior recall, identificando mais clientes com risco de cancelamento e reduzindo a quantidade de falsos negativos.

Do ponto de vista de negócio, isso é importante porque ajuda a empresa a agir antes que o cliente cancele.

## Melhor modelo até o momento

Random Forest Ajustado:

- Recall: 0.79
- ROC-AUC: 0.84
- Falsos negativos: 79
- Verdadeiros positivos: 295

## Ferramentas utilizadas

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
