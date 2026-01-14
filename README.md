
# Customer Churn Prediction & Business Impact Analysis

Este projeto apresenta uma solução para a previsão de evasão de clientes (customer churn) em uma empresa fictícia de telecomunicações. O objetivo central é identificar clientes com alto risco de cancelamento, permitindo a adoção de estratégias preventivas de retenção, com impacto direto na redução de perdas financeiras.


## Problema de Negócio

A evasão de clientes representa um dos principais desafios para empresas baseadas em assinatura, uma vez que o custo de aquisição de novos clientes é significativamente maior do que o custo de retenção.

---

## Objetivos

* Construir um modelo preditivo para identificar clientes com alto risco de evasão
* Comparar diferentes algoritmos de classificação
* Interpretar os fatores determinantes do churn
* Simular o impacto financeiro do uso do modelo na estratégia de retenção

---

## Dataset

* Dataset público **Telco Customer Churn**
* Contém informações:

  * Demográficas
  * Contratuais
  * Financeiras
  * Comportamentais
* Variável alvo binária indicando churn (Yes/No)
---

## Metodologia

### Análise Exploratória de Dados (EDA)

* Distribuição da variável alvo
* Análise de churn por:

  * Tipo de contrato
  * Tempo de permanência (tenure)
  * Valor mensal
  * Forma de Pagamento
  * Serviços

---

### Preparação dos Dados

* Tratamento de valores ausentes
* Codificação de variáveis categóricas
* Normalização de variáveis numéricas
* Feature engineering 

---

### Modelagem

Foram avaliados diferentes modelos de classificação, incluindo:

* Regressão Logística
* Random Forest
* Gradient Boosting 

Cada modelo foi treinado utilizando divisão adequada entre treino e teste, respeitando boas práticas de validação.

---

### Avaliação dos Modelos

As métricas utilizadas foram Recall, Precision, F1-Score e ROC-AUC, com ênfase especial em Recall, uma vez que não identificar um cliente que irá evadir gera maior prejuízo do que um falso positivo.

**Métricas avaliadas:**

* Recall
* Precision
* F1-score
* ROC-AUC

---

## Resultados Obtidos e Escolha do Modelo Final

O modelo final foi selecionado com base no melhor Recall, pois este apresenta melhor equilíbrio geral entre desempenho e interpretabilidade. Embora modelos baseados em árvores apresentem maior precisão, eles falham em capturar uma parcela significativa dos clientes que realmente evadem.

Resultados:
<img width="798" height="183" alt="image" src="https://github.com/user-attachments/assets/8a4f7d14-6f19-42cb-8dde-31939b6ec477" />

---

## Simulação de Impacto de Negócio

A partir das probabilidades previstas pelo modelo:

* Clientes foram classificados em faixas de risco
* Simulou-se uma estratégia de retenção focada no grupo de maior risco

Resultados indicam:

Público Alvo da Campanha: 877 clientes (identificados pelo modelo).

Receita em Risco Detectada: $ 67,145.55 (Valor mensal dos contratos em perigo).

Taxa de Sucesso Estimada: 30% (Clientes que aceitam a oferta e ficam).

---

## Tecnologias Utilizadas

* Python
* Pandas / NumPy
* Scikit-learn
* Matplotlib / Seaborn
* Jupyter Notebook
* Git/GitHub

---

## Conclusão

O projeto demonstra como **modelos de Machine Learning aliados à interpretabilidade** podem apoiar decisões estratégicas em negócios reais. A solução proposta equilibra **desempenho preditivo e transparência**, permitindo não apenas prever churn, mas também compreender seus principais determinantes.

A simulação de negócio validou essa abordagem ao projetar um retorno líquido mensal superior a $ 13.000, evidenciando que, mesmo após deduzir custos operacionais e descontos de incentivo, o modelo atua como uma ferramenta financeira robusta capaz de otimizar o orçamento de marketing e proteger a receita da empresa de forma lucrativa e direcionada.
